---
title: FIFOs - First In First Out
subtitle: Post on FIFOs - First In First Out

# Summary for listings and search engines
summary: Post on FIFOs - First In First Out

# Link this post with a project
projects: []

# Date published
date: '2020-12-13T00:00:00Z'

# Date updated
lastmod: '2020-12-13T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Academic

categories:
  - Demo
---

## Introduction

The Linux IPC (Inter-process communication) system provides a means for processes to communicate with each other.

There are several IPC methods available to programmers:

   - half-duplex UNIX channels
   - FIFO (named pipes)
   - SYSV style message queues
   - Multiple SYSV-style semaphores
   - SYSV style shared memory segments
   - Network sockets (Berkeley style) (not covered by this article)
   - Full duplex channels (stream channels) (not covered by this article)

If used effectively, these features provide a solid base for maintaining a client/server ideology on any UNIX system, including Linux.

## Basic concepts

Named pipes work in much the same way as regular pipes, but still have a few notable differences.

    Named pipes exist as a special device file in the file system.
    Processes of different origins can share data through such a channel.
    The named pipe remains on the file system for later use after all I/O is done.


### Create FIFO

There are several ways to create a named pipe. The first two can be done directly from the shell.

```

mknod MYFIFO p
mkfifo a=rw MYFIFO

```

These two commands perform identical operations, with one exception. The mkfifo command provides the ability to change the permissions of a FIFO file immediately after creation. When using mknod, a call to the chmod command will be required.

FIFO files can be quickly identified in the physical file system by the "p" indicator, shown here in the long directory listing.

```

$ ls -1 MYFIFO
^prw-r--r-- 1 root root 0 Dec 14 22:15 MYFIFO| ...

```

Also note that the vertical separator is placed directly after the filename. Another good reason to run

```

Linux, huh?

```

To create a FIFO in C, we can resort to using the mknod() system call:

```

LIBRARY FUNCTION: mknod();
PROTOTYPE: int mknod( char *pathname, mode_t mode, dev_t dev );
   RETURNS: 0 on success,
            -1 on error:
               errno = EFAULT (wrong path specified)
                       EACCESS (no rights)
                       ENAMETOOLONG (way too long)
                       ENOENT (wrong path specified)
                       ENOTDIR (wrong path specified)
                       (see the mknod man page for the rest)
     NOTES: Creates a file system node (file, device file, or
FIFO)

```

We leave the more detailed discussion of the mknod() man page, but for now let's look at a simple example of creating a FIFO in C:

```

   mknod("/tmp/MYFIFO", S_IFIFO|0666, 0);

```

In this case, the file "/tmp/MYFIFO" is created as a FIFO file. The permissions required are "0666", although they are influenced by the umask setting, such as:

```

   final_umask = requested_permissions & ~original_umask ...

```

A general trick is to use the umask() system call to temporarily remove the umask value:

```

   umask(0);
   mknod("/tmp/MYFIFO", S_IFIFO|0666, 0);

```

Also, the third argument to mknod() is ignored, otherwise we create a device file. In this case, it should note the top and bottom numbers of the device file.

## FIFO operations

FIFO I/O operations are essentially the same as for regular channels, with one exception. To physically open a passage to a channel, the "open" system call or library function must be used. With half-duplex pipes, this is not possible because the pipe resides in the kernel and not in the physical file system. In our example, we will treat the channel as a stream, opening it with fopen() and closing it with fclose().

Consider a simple server process:

```

/***************************************************** ***************************
 Excerpt from "Linux Programmer's Guide - Chapter 6"
 (C)opyright 1994-1995, Scott Burkett
 ******************************************************* **************************
 MODULE: fifoserver.c
 ******************************************************* **************************
#include
#include #include
#include
#include
#define FIFO_FILE "MYFIFO"
int main(void)
{
   FILE *fp;
   char readbuf[80];
   /* Create FIFO if it doesn't already exist */
   umask(0);
   mknod(FIFO_FILE, S_IFIFO|0666, 0);
   while(1)
   {
      fp = fopen(FIFO_FILE, "r");
      fgets(readbuf, 80, fp);
      printf("Received string: %s\n", readbuf);
      fclose(fp);
   }
   return(0);
}

```

Since FIFO blocks by default, let's start the server in the background after it has been compiled:

```

   $fifoserver&

```

We'll discuss the blocking action shortly, but first let's look at the following simple client for our server:

```

/***************************************************** ***************************
 Excerpt from "Linux Programmer's Guide - Chapter 6"
 (C)opyright 1994-1995, Scott Burkett
 ******************************************************* **************************
 MODULE: fifoclient.c
 ******************************************************* **************************
#include
#include
#define FIFO_FILE "MYFIFO"int main(int argc, char *argv[])
{
   FILE *fp;
   if ( argc != 2 ) {
      printf("USAGE: fifoclient [string]\n");
      exit(1);
   }
   fputs(argv[1], fp);
   fclose(fp);
   return(0);
}
```

## Blocking action on FIFO

If the FIFO is open for reading, the process blocks until some other process opens the FIFO for writing. Similarly for the reverse situation. If this behavior is not desired, then the O_NONBLOCK flag in the open() system call can be used to cancel the blocking action.

In our simple server example, we just put it in the background and let it block there. An alternative would be to jump to another virtual console and start the client, switching back and forth to see the result.
