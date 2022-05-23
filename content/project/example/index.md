---
title: Реализация класса векторов на c++ 
summary: Проект посвящен созданию упрощённого класса векторов на языке программирования c++.
tags:
  - Deep Learning
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
  - icon: twitter
    icon_pack: fab
    name: Follow
    url: https://twitter.com/georgecushen
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

Что нужно знать для реализации?

- Указатели

- Move семантика (Дополнительный этап)

- rValue и lValue ссылки (Дополнительный этап)

- Шаблоны

- Итераторы (Дополнительный этап)

- Переопределение операторов

Класс Vector должен иметь следующие поля рrivate : 
- Размерность вектора
- Массив значений вектора
- Порядковый номер вектора
Класс Vестоr должен иметь следующие поля public :
- Количество созданных векторов ( static ) 

 Необходимо реализовать следующие функции или методы класса: 
 
- Набор конструкторов класса, включающий конструктор копирования 
- Деструктор • Функция отображения вектора и его номера ( print ) 
- Оператор - функции : 
 - сложения / вычитания векторов
 - унарный минус 
 - скалярного произведения векторов
 - присваивания
