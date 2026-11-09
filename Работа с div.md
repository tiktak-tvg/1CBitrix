### Работа с div
Что такое ``<div>``?

``<div> (от англ. division — «раздел»)`` — универсальный блочный контейнер без смысловой нагрузки. Используется для группировки элементов, чтобы:

- применить к ним общие стили через класс или ``id``;
- расположить элементы в нужном порядке;
- создать каркас страницы (шапка, контент, подвал, колонки, карточки).
- <div> сам по себе ничего не значит: ни заголовок, ни абзац, ни статья. Он просто «коробка» для других элементов.

Синтаксис

```html
<div>Содержимое</div>
```
С атрибутами:
```html
<div class="card" id="main-card">
  Содержимое
</div>
```
#### Ключевые свойства <div>

По умолчанию ``<div>``:
- блочный ``(display: block)`` — занимает всю ширину родителя, начинает новую строку;
- не имеет собственных отступов, рамок и фона — всё задаётся через CSS.

#### Типичные CSS-свойства для <div>:
```css
.box {
  width: 300px;              /* ширина */
  height: 150px;             /* высота */
  padding: 16px;             /* внутренний отступ */
  margin: 12px;              /* внешний отступ */
  background: #f7f9fb;       /* фон */
  border: 1px solid #ddd;    /* рамка */
  border-radius: 8px;        /* скругление углов */
  color: #333;               /* цвет текста */
  box-shadow: 0 2px 8px rgba(0,0,0,.06);
}
```
#### Пример 1. Простой блок с текстом
```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>div — простой блок</title>
  <style>
    .box {
      width: 300px;
      padding: 16px;
      margin: 20px auto;
      background: #f7f9fb;
      border: 1px solid #ddd;
      border-radius: 8px;
    }
  </style>
</head>
<body>
  <div class="box">
    Это простой блок div с текстом внутри. Стили заданы через класс.
  </div>
</body>
</html>
```
Результат: аккуратная «коробка» по центру страницы с белым фоном, рамкой и скруглёнными углами.

#### Пример 2. Каркас страницы (шапка, контент, подвал)
```html
<body>
  <div class="header">Шапка сайта</div>
  <div class="content">Основной контент</div>
  <div class="footer">Подвал сайта</div>
</body>
css
.header  { background: #2c3e50; color: white; padding: 20px; }
.content { background: #f4f4f4; padding: 20px; min-height: 200px; }
.footer  { background: #34495e; color: white; padding: 16px; }
```
Это классическая схема «шапка — контент — подвал». В современном HTML вместо ``<div>`` для этих блоков лучше использовать семантические теги ``<header>, <main>, <footer>`` — они делают разметку понятнее.

#### Пример 3. Вложенные <div>
``<div>`` можно вкладывать друг в друга — так строят карточки, колонки, сетки.
```html
<div class="card">
  <div class="card-header">
    <h2>Заголовок карточки</h2>
  </div>
  <div class="card-body">
    <p>Текст карточки.</p>
  </div>
  <div class="card-footer">
    <a href="#">Подробнее</a>
  </div>
</div>
css
.card {
  max-width: 400px;
  border: 1px solid #ddd;
  border-radius: 12px;
  overflow: hidden;
  background: white;
}

.card-header {
  background: #3498db;
  color: white;
  padding: 12px 16px;
}

.card-body {
  padding: 16px;
}

.card-footer {
  background: #f4f4f4;
  padding: 12px 16px;
  border-top: 1px solid #ddd;
}
```
Результат: карточка с цветной шапкой, текстом и подвалом. Каждая часть — отдельный ``<div>``.

#### Пример 4. Колонки через ``display: flex``
```html
<div class="row">
  <div class="col">Колонка 1</div>
  <div class="col">Колонка 2</div>
  <div class="col">Колонка 3</div>
</div>
css
.row {
  display: flex;      /* включает flex-раскладку */
  gap: 16px;          /* расстояние между колонками */
}

.col {
  flex: 1;            /* все колонки одинаковой ширины */
  padding: 16px;
  background: #f7f9fb;
  border: 1px solid #ddd;
  border-radius: 8px;
  text-align: center;
}
```
Результат: три равные колонки в один ряд. ``display: flex`` на родителе — современный способ строить ряды из ``<div>``.

#### Пример 5. ``<div>`` как сетка карточек
```html
<div class="grid">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);  /* 3 колонки */
  gap: 12px;
}

.item {
  background: #3498db;
  color: white;
  padding: 24px;
  text-align: center;
  border-radius: 8px;
}
```
Результат: сетка 3×2 из шести квадратов.

#### Пример 6. ``<div>`` для скрытия и показа блоков
Свойство ``display`` управляет отображением:

```html
<div class="visible">Видимый блок</div>
<div class="hidden">Скрытый блок</div>
css
.visible {
  background: #e8f5e9;
  padding: 12px;
}

.hidden {
  display: none;   /* полностью убирает из потока */
}
```
Позже через ``JavaScript`` можно поменять ``display: none на display: block`` и показать блок.

Есть ещё ``visibility:``

```css
.invisible {
  visibility: hidden;  /* элемент невидим, но место занимает */
}
```

Разница:

``display: none`` — элемент полностью исчезает, место не занимает;

``visibility: hidden`` — элемент невидим, но оставляет пустое место.

#### Пример 7. ``<div> vs <span>``

Тег   	|Тип	   |Где использовать
  ----- | --------| ---------------------------------------------
``<div>``	 |Блочный	 |Группировка блоков, каркас страницы
``<span>``	 |Строчный	 |Выделение части текста в строке

```html
<div class="card">
  <p>Текст с <span class="highlight">выделенным словом</span> внутри.</p>
</div>
<div> начинает новую строку и занимает всю ширину;
<span> не разрывает строку, занимает ширину по содержимому.
```
#### Пример 8. ``<div> vs`` семантические теги

В HTML5 есть смысловые контейнеры, которые лучше ``<div>``, когда у блока есть конкретная роль:

Тег	|Роль
---- | -----------
``<header>``	 |Шапка страницы или раздела
``<nav>``	 |Навигация (меню)
``<main>``	 |Основной контент
``<section>``	 |Смысловой раздел
``<article>``	 |Статья, карточка новости
``<aside>``	 |Боковая врезка
``<footer>``	 |Подвал

Когда роль неочевидна или блок нужен только для оформления — используют ``<div>``.

Плохо:
```html
<div class="header">...</div>
<div class="nav">...</div>
<div class="main">...</div>
```
Хорошо:
```html
<header>...</header>
<nav>...</nav>
<main>...</main>
```
Типичные ошибки
``<div>`` вместо ``<p>`` для абзаца текста

```html
<div>Просто абзац текста</div>
```
Лучше: 
``<p>Просто абзац текста</p>``.

#### Пример 9. ``<div>`` вокруг каждой ссылки или слова

```html
<div><a href="#">Ссылка</a></div>
```
Для строчных элементов внутри текста используйте ``<span>``, а блочные контейнеры — только когда нужна группировка.

Слишком много ``<div>`` без причины

Если блок нужен только для переноса или отступа — часто достаточно margin или gap.

``<div> с id`` в нескольких местах

id должен быть уникальным. Для повторяющихся карточек — только классы.

Вложенность ``<div>`` ради вложенности

Если ``<div>`` не несёт смысла и не нужен для стилей — уберите его.

Готовая демонстрационная страница
```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Работа с div</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 900px;
      margin: 40px auto;
      padding: 0 16px;
      color: #222;
      background: #f4f4f4;
    }

    h1 {
      color: #2c3e50;
      text-align: center;
    }

    h2 {
      color: #34495e;
      margin-top: 32px;
    }

    /* Каркас */
    .header {
      background: #2c3e50;
      color: white;
      padding: 20px;
      border-radius: 8px 8px 0 0;
    }

    .content {
      background: white;
      padding: 20px;
    }

    .footer {
      background: #34495e;
      color: white;
      padding: 16px;
      border-radius: 0 0 8px 8px;
    }

    /* Карточка */
    .card {
      border: 1px solid #ddd;
      border-radius: 12px;
      overflow: hidden;
      background: white;
      margin: 16px 0;
    }

    .card-header {
      background: #3498db;
      color: white;
      padding: 12px 16px;
    }

    .card-body {
      padding: 16px;
    }

    .card-footer {
      background: #f4f4f4;
      padding: 12px 16px;
      border-top: 1px solid #ddd;
    }

    /* Ряд колонок */
    .row {
      display: flex;
      gap: 16px;
      margin: 16px 0;
    }

    .col {
      flex: 1;
      padding: 16px;
      background: #eef2f5;
      border: 1px solid #ddd;
      border-radius: 8px;
      text-align: center;
    }

    /* Сетка */
    .grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
    }

    .item {
      background: #3498db;
      color: white;
      padding: 24px;
      text-align: center;
      border-radius: 8px;
    }

    /* Скрытый блок */
    .hidden {
      display: none;
    }
  </style>
</head>
<body>

  <h1>Работа с div</h1>

  <h2>1. Каркас страницы</h2>
  <div class="header">Шапка сайта</div>
  <div class="content">
    Основной контент страницы. Внутри может быть любой HTML.
  </div>
  <div class="footer">Подвал сайта</div>

  <h2>2. Карточка с вложенными div</h2>
  <div class="card">
    <div class="card-header">
      <h3>Заголовок карточки</h3>
    </div>
    <div class="card-body">
      <p>Текст карточки с вложенными блоками.</p>
    </div>
    <div class="card-footer">
      <a href="#">Подробнее</a>
    </div>
  </div>

  <h2>3. Колонки через flex</h2>
  <div class="row">
    <div class="col">Колонка 1</div>
    <div class="col">Колонка 2</div>
    <div class="col">Колонка 3</div>
  </div>

  <h2>4. Сетка через grid</h2>
  <div class="grid">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
    <div class="item">6</div>
  </div>

  <h2>5. Скрытый блок</h2>
  <div class="hidden">Этот блок не отображается (display: none)</div>
  <p>Скрытый блок выше есть в HTML, но не виден.</p>

</body>
</html>
```
Итоговая шпаргалка
```html
<!-- Простой контейнер -->
<div>Содержимое</div>

<!-- С классом и id -->
<div class="card" id="main-card">...</div>

<!-- Вложенные блоки -->
<div class="card">
  <div class="card-header">...</div>
  <div class="card-body">...</div>
</div>

<!-- Колонки -->
<div class="row">
  <div class="col">1</div>
  <div class="col">2</div>
</div>
css
/* Типичные стили для div */
.box {
  width: 300px;
  padding: 16px;
  margin: 0 auto;            /* центрирование */
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 8px;
}

.row  { display: flex; gap: 16px; }   /* колонки */
.grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; }
.hidden { display: none; }
```
Ключевые правила:

``<div>`` — только для группировки блоков, не для текста.

Для смысловых блоков используйте ``<header>, <main>, <footer>, <section>, <article>``.

``<div>`` не разрывает строку — он блочный и всегда начинает новую.

Стили задавайте через классы, а не через id (если блок повторяется).

Не вкладывайте <div> «на всякий случай» — только когда это нужно для стилей или структуры.

