### Знакомство с HTML, CSS
- Знакомство с HTML
- Синтаксис тегов
- Список тегов
- HTML-атрибуты
- Вложенные теги
- Исходная структура страницы
- Meta-теги
- Задание
- Решение
- Знакомство с CSS
- Переходим к стилям
- Знакомство с CSS
- Страница со стилями
- Основные CSS-свойства
- Способы внедрения стилей
- Абсолютные и относительные пути
- Работа со стилями
- Задание
- Подсказка

<img width="1371" height="774" alt="image" src="https://github.com/user-attachments/assets/fe077fbb-7a20-47aa-a9dc-c91ea0a99336" />

#### Знакомство с HTML
Описание: HTML — язык разметки, который задаёт структуру страницы: заголовки, абзацы, ссылки, картинки, списки. HTML не оформляет внешний вид — за это отвечает CSS.

Пример:

```html
<h1>Моя первая страница</h1>
<p>Это абзац текста.</p>
<a href="https://example.com">Ссылка</a>
```
#### Синтаксис тегов
Описание: Тег — команда в угловых скобках. Бывают парные теги: ``<p>...</p>`` и одиночные: ``<img>, <br>, <hr>``. У тега могут быть атрибуты.

Пример:

```html
<p>Парный тег с текстом</p>
<img src="cat.jpg" alt="Кот">
<br>
```
Общая схема:

```html
<тег атрибут="значение">содержимое</тег>
```
#### Список тегов
Описание: Основные теги задают каркас и содержимое страницы.

Тег	|Назначение	|Пример
---- | --------- | ---------------
``<html>``	 |Корень документа	 |``<html lang="ru">...</html>``
``<head>``	 |Служебная информация	 |``<head><title>Сайт</title></head>``
``<body>``	 |Видимое содержимое	 |``<body><h1>Привет</h1></body>``
``<title>``	 |Заголовок вкладки	 |``<title>Мой сайт</title>``
``<h1>…<h6>``	 |Заголовки	 |``<h1>Главный</h1>``
``<p>``	 |Абзац	 |``<p>Текст</p>``
``<a>``	 |Ссылка	 |``<a href="/about">О нас</a>``
``<img>``	 |Изображение	 |``<img src="cat.jpg" alt="Кот">``
``<ul>, <ol>, <li>``	 |Списки	 |``<ul><li>HTML</li></ul>``
``<div>``	 |Блочный контейнер	 |``<div class="card">...</div>``
``<span>``	 |Строчный контейнер	 |``<span>текст</span>``
``<strong>, <em>``	 |Важность/акцент	 |``<strong>важно</strong>``
``<header>, <main>, <footer>``	 |Семантические блоки	 |``<main>...</main>``

#### HTML-атрибуты
Описание: Атрибуты уточняют поведение тега. Бывают глобальные ``(id, class, title, style)`` и специальные ``(href, src, alt, type)``.

Пример:

```html
<a href="https://example.com" target="_blank" title="Открыть сайт">
  Пример сайта
</a>

<img src="images/cat.jpg" alt="Рыжий кот" width="200">

<p id="intro" class="text important">Текст с id и классами</p>
```
#### Вложенные теги
Описание: Теги можно вкладывать друг в друга. Важно закрывать их в обратном порядке.

Пример:

```html
<div class="card">
  <h2>Заголовок карточки</h2>
  <p>Текст с <strong>важным</strong> словом.</p>
  <ul>
    <li>Пункт 1</li>
    <li>Пункт 2</li>
  </ul>
</div>
```
Правильно: ``<p><strong>текст</strong></p>``.

Неправильно: ``<p><strong>текст</p></strong>``.

#### Исходная структура страницы
Описание: Минимальный каркас HTML-документа: ``DOCTYPE, html, head, body``.

Пример:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Моя страница</title>
</head>
<body>
  <h1>Привет, мир!</h1>
  <p>Это моя первая страница.</p>
</body>
</html>
```
#### Meta-теги
Описание: Meta-теги находятся в ``<head>`` и передают браузеру и поисковикам служебную информацию: кодировку, адаптивность, описание, автора.

Пример:

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Учебная страница по HTML и CSS">
  <meta name="keywords" content="HTML, CSS, обучение">
  <meta name="author" content="Иван Иванов">
  <meta name="robots" content="index, follow">
  <title>Учебная страница</title>
</head>
```
#### Задание по HTML
Описание: Создайте страницу с заголовком, абзацем, изображением, списком, ссылкой и meta-тегами.

Задание:
- Создайте файл ``index.html``.
- Добавьте каркас страницы.
- В ``<head>`` укажите кодировку, ``viewport``, описание и ``title``.
- В ``<body>`` добавьте:
- ``h1``;
- абзац с ``strong и em``;
- изображение;
- список;
- ссылку.

#### Решение задания по HTML
Пример:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Моя первая учебная страница">
  <title>Моя первая страница</title>
</head>
<body>
  <header>
    <h1>Привет, мир!</h1>
    <nav>
      <a href="#about">Обо мне</a> |
      <a href="#contacts">Контакты</a>
    </nav>
  </header>

  <main>
    <section id="about">
      <h2>Обо мне</h2>
      <p>Я учусь <strong>HTML</strong> и <em>CSS</em>.</p>
      <img src="images/cat.jpg" alt="Рыжий кот" width="200">
      <ul>
        <li>HTML</li>
        <li>CSS</li>
      </ul>
    </section>
  </main>

  <footer id="contacts">
    <p>Связаться: <a href="mailto:test@example.com">test@example.com</a></p>
  </footer>
</body>
</html>
```
#### Знакомство с CSS
Описание: CSS — язык стилей. Он описывает, как HTML-элементы выглядят: цвет, шрифт, отступы, рамки, расположение.

Синтаксис:

```css
селектор {
  свойство: значение;
}
```
Пример:

```css
p {
  color: darkblue;
  font-size: 18px;
}
```
11. Переходим к стилям
Описание: HTML отвечает за структуру, CSS — за оформление. Один и тот же HTML можно оформить по-разному.

Пример HTML без CSS:

```html
<h1>Заголовок</h1>
<p>Текст страницы.</p>
```
Пример с CSS:

```css
h1 {
  color: white;
  background: #2c3e50;
  padding: 16px;
}

p {
  font-family: Arial, sans-serif;
  line-height: 1.5;
}
```
#### Страница со стилями
Описание: Стили можно добавить прямо в HTML через тег ``<style>``.

Пример:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Страница со стилями</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      color: #222;
      margin: 0;
      padding: 20px;
    }

    h1 {
      color: #2c3e50;
    }

    .card {
      background: white;
      padding: 16px;
      border: 1px solid #ddd;
      border-radius: 8px;
    }
  </style>
</head>
<body>
  <h1>Страница со стилями</h1>
  <div class="card">
    <p>Этот блок оформлен через CSS.</p>
  </div>
</body>
</html>
```
#### Основные CSS-свойства
Описание: Часто используемые свойства:

Свойство	|Пример	|Что делает
---- | --------- | ---------------
``color``	 |``color: red;``	 |Цвет текста
``background-color``	 |``background-color: #eee;``	 |Цвет фона
``font-size``	 |``font-size: 18px;``	 |Размер шрифта
``font-family``	 |``font-family: Arial, sans-serif;``	 |Шрифт
``font-weight``	 |``font-weight: bold;``	 |Жирность
``text-align``	 |``text-align: center;``	 |Выравнивание текста
``margin``	 |``margin: 20px;``	 |Внешний отступ
``padding`` |	``padding: 16px;``	 |Внутренний отступ
``border``	 |``border: 1px solid #ccc;``	 |Рамка
``width, height``	 |``width: 200px;``	 |Размеры
``border-radius``	 |``border-radius: 8px;``	 |Скругление углов
``display``	 |``display: flex;``	 |Тип отображения

Пример:

```css
.card {
  background-color: white;
  color: #222;
  padding: 16px;
  border: 1px solid #ddd;
  border-radius: 8px;
  width: 300px;
}
```
#### Способы внедрения стилей
Описание: Есть три основных способа.

1. Внешний файл — лучший способ
```html
<link rel="stylesheet" href="css/styles.css">
css/styles.css:
```

```css
body {
  background: #f5f5f5;
}
```
2. Внутренние стили в <head>
```html
<style>
  h1 {
    color: green;
  }
</style>
```
3. Встроенные стили в атрибуте style
```html
<p style="color: red; font-size: 18px;">Красный текст</p>
```
Внешний файл удобнее: стили переиспользуются и не смешиваются с HTML.

#### Абсолютные и относительные пути
Описание: Путь указывает, где находится файл: картинка, стиль, страница.

Абсолютные пути
Начинаются с / от корня сайта или с полного URL:

```html
<link rel="stylesheet" href="/css/styles.css">
<img src="https://example.com/images/cat.jpg" alt="Кот">
```
Относительные пути
Считаются от текущего файла:

```html
<link rel="stylesheet" href="css/styles.css">
<img src="images/cat.jpg" alt="Кот">
<img src="../images/cat.jpg" alt="Кот">
```
Пояснение:

``css/styles.css`` — файл в папке css рядом с HTML;

``../images/cat.jpg`` — подняться на уровень выше и зайти в images;

``./styles.css`` — файл в той же папке.

#### Работа со стилями
Описание: В CSS важно понимать селекторы, каскад, специфичность и наследование.

Пример селекторов:

```css
p {
  color: #333;
}

.card {
  padding: 16px;
}

#main-title {
  color: #2c3e50;
}
```
Пример каскада:

```css
p {
  color: blue;
}

.text {
  color: green;
}
html
<p class="text">Этот текст будет зелёным</p>
```
Класс ``.text`` имеет больший приоритет, чем селектор тега p.

Полезно:
- использовать классы для повторяющихся стилей;
- проверять стили через DevTools браузера;
- подключать внешний CSS;
- не злоупотреблять !important.

#### Задание по CSS
Описание: Подключите внешний CSS к HTML-странице и оформите её.

Задание:
- Создайте файл ``styles.css``.
- Подключите его в ``index.html`` через ``<link>``.

Сделайте:
- светлый фон страницы;
- заголовок h1 тёмно-синим;
- ссылки без подчёркивания;
- карточку с белым фоном, отступами, рамкой и скруглением;
- изображение с рамкой.

#### Подсказка
Описание: Проверьте подключение CSS и используйте классы.

Пример подсказки:

```html
<link rel="stylesheet" href="styles.css">
html
<div class="card">
  <h2>Заголовок</h2>
  <p>Текст карточки.</p>
</div>
css
body {
  background: #f4f4f4;
  font-family: Arial, sans-serif;
}

h1 {
  color: #2c3e50;
}

a {
  text-decoration: none;
}

.card {
  background: white;
  padding: 16px;
  border: 1px solid #ddd;
  border-radius: 8px;
}

img {
  border: 3px solid #2c3e50;
  border-radius: 8px;
}
```
Если стили не применились, проверьте:
- путь в ``href``;
- имя файла ``styles.css``;
- что ``<link>`` находится в ``<head>``;
- нет ли опечаток в CSS;
- не перекрывают ли стили друг друга.

### Знакомство с CSS: свойства, способы внедрения стилей, пути
#### Основные CSS-свойства
##### 1. ``color`` — цвет текста
Описание: Задаёт цвет текста элемента. Можно указывать именованные ``цвета, HEX, rgb(), rgba(), hsl()``.

Пример:
```css
p {
  color: #2c3e50;      /* тёмно-синий */
}

h1 {
  color: darkred;       /* именованный цвет */
}

a {
  color: rgb(0, 123, 255);
}
```

---

```html
<p>Тёмно-синий текст</p>
<h1>Тёмно-красный заголовок</h1>
<a href="#">Синяя ссылка</a>
```
##### 2. ``background-color`` — фоновый цвет
Описание: Задаёт цвет фона элемента. Фон заполняет область контента и внутренних отступов ``(padding)``, но не внешних ``(margin)``.

Пример:
```css
body {
  background-color: #f4f4f4;
}

.card {
  background-color: white;
}

.alert {
  background-color: #ffe5e5;
  color: #b00020;
}
```

---

```html
<div class="card">Карточка на белом фоне</div>
<div class="alert">Предупреждение</div>
```
##### 3. ``background-imag``e — фоновое изображение
Описание: Устанавливает картинку как фон элемента. Часто используется вместе с ``background-size, background-repeat, background-position.``

Пример:
```css
.hero {
  background-image: url("images/hero.jpg");
  background-size: cover;       /* картинка заполняет блок */
  background-position: center;  /* центрирование */
  background-repeat: no-repeat; /* без повторов */
  height: 300px;
  color: white;
}
```

---

```html
<section class="hero">
  <h1>Добро пожаловать</h1>
</section>
```
Короткая запись:

```css
.hero {
  background: url("images/hero.jpg") center / cover no-repeat;
}
```
##### 4. ``font-size`` — размер шрифта
Описание: Устанавливает размер текста. Можно задавать в ``px, em, rem, %, vw`` и других единицах.

Пример:
```css
body {
  font-size: 16px;   /* базовый размер */
}

h1 {
  font-size: 2rem;   /* 32px, если базовый 16px */
}

.small {
  font-size: 0.875em; /* 14px */
}

.big {
  font-size: 24px;
}
```

---

```html
<h1>Большой заголовок</h1>
<p class="small">Мелкий текст</p>
<p class="big">Крупный текст</p>
```
##### 5. ``font-style`` — стиль начертания
Описание: Управляет начертанием: обычное, курсивное, наклонное.

Значения:

normal — обычное (по умолчанию);

italic — курсив;

oblique — наклонное.

Пример:
```css
.normal  { font-style: normal; }
.italic  { font-style: italic; }
.oblique { font-style: oblique; }
```

---

```html
<p class="normal">Обычный текст</p>
<p class="italic">Курсивный текст</p>
<p class="oblique">Наклонный текст</p>
```
##### 6. ``font-family`` — семейство шрифтов
Описание: Задаёт шрифт для текста. Указывается список шрифтов через запятую — браузер берёт первый доступный. Последним обычно указывают общее семейство ``(serif, sans-serif, monospace)``.

Пример:
```css
body {
  font-family: Arial, Helvetica, sans-serif;
}

h1 {
  font-family: Georgia, "Times New Roman", serif;
}

code {
  font-family: "Courier New", monospace;
}
```

---

```html
<h1>Заголовок с засечками</h1>
<p>Основной текст без засечек</p>
<code>моноширинный код</code>
```
##### 7. ``text-align`` — горизонтальное выравнивание текста
Описание: Выравнивает текст внутри блочного элемента.

Значения:
- ``left`` — по левому краю;
- ``right`` — по правому;
- ``center`` — по центру;
- ``justify`` — по ширине (с растягиванием пробелов).

Пример:

```css
.left    { text-align: left; }
.center  { text-align: center; }
.right   { text-align: right; }
.justify { text-align: justify; }
```

---

```html
<p class="center">Текст по центру</p>
<p class="right">Текст справа</p>
<p class="justify">Длинный текст, растянутый по ширине блока...</p>
```
##### 8. ``text-transform`` — преобразование регистра
Описание: Управляет регистром символов текста.

Значения:
- ``none`` — без изменений;
- ``uppercase`` — ВСЕ ЗАГЛАВНЫЕ;
- ``lowercase`` — все строчные;
- ``capitalize`` — Каждое Слово С Заглавной.

Пример:
```css
.upper { text-transform: uppercase; }
.lower { text-transform: lowercase; }
.cap   { text-transform: capitalize; }
html
<p class="upper">привет мир</p>   <!-- ПРИВЕТ МИР -->
<p class="lower">ПРИВЕТ МИР</p>   <!-- привет мир -->
<p class="cap">привет мир</p>     <!-- Привет Мир -->
```
##### 9. border-color — цвет рамки
Описание: Задаёт цвет всех четырёх сторон рамки. Работает только если задан ``border-style (например, solid)``.

Пример:
```css
.box {
  border-style: solid;
  border-width: 2px;
  border-color: #2c3e50;
}

.box-red {
  border: 2px solid red; /* короткая запись */
}
```

---

```html
<div class="box">Рамка с цветом #2c3e50</div>
<div class="box-red">Красная рамка</div>
```
Можно задать разные цвета сторон:
```css
.box {
  border-style: solid;
  border-width: 2px;
  border-color: red green blue orange; /* верх право низ лево */
}
```
##### 10. border-radius — скругление углов
Описание: Устанавливает радиус скругления углов рамки. Применяется и к фону, и к рамке, и к изображению.

Пример:
```css
.small-radius {
  border-radius: 4px;
}

.card {
  border: 1px solid #ddd;
  border-radius: 12px;
}

.circle {
  width: 100px;
  height: 100px;
  border-radius: 50%; /* круг */
  background: #3498db;
}
```

---

```html
<div class="card">Карточка со скруглёнными углами</div>
<div class="circle"></div>
```
Можно задать разные радиусы:

```css
.box {
  border-radius: 10px 20px 30px 40px; /* по часовой стрелке от верхнего левого */
}
```
##### 11. margin — внешний отступ
Описание: Отступ снаружи элемента — расстояние между элементом и соседними элементами. Не входит в область фона.

Пример:
```css
.box {
  margin: 20px;              /* со всех сторон */
}

.box-2 {
  margin: 10px 20px;         /* верх/низ 10px, право/лево 20px */
}

.box-3 {
  margin: 0 auto;            /* центрирование блока по горизонтали */
  width: 300px;
}
html
<div class="box">Отступ 20px со всех сторон</div>
<div class="box-3">Блок по центру</div>
```
##### 12. padding — внутренний отступ
Описание: Отступ внутри элемента — расстояние между содержимым и рамкой/границей. Входит в область фона.

Пример:
```css
.card {
  background: white;
  padding: 16px;
  border: 1px solid #ddd;
}

.btn {
  padding: 10px 20px;        /* 10px сверху/снизу, 20px по бокам */
  background: #3498db;
  color: white;
}
html
<div class="card">Текст с внутренним отступом 16px</div>
<button class="btn">Кнопка</button>
```
Разница margin и padding:

- ``padding`` — внутри рамки, добавляет «воздух» вокруг текста;
- ``margin`` — снаружи, отталкивает соседние элементы.

##### 13. display — отображение элемента
Описание: Определяет, как элемент ведёт себя в потоке документа.

Основные значения:
- ``block`` — блочный (занимает всю ширину, переносит на новую строку);
- ``inline`` — строчный (в потоке текста, ширина по содержимому);
- ``inline-block`` — строчный, но с размерами как у блочного;
- ``flex`` — флекс-контейнер;
- ``grid`` — грид-контейнер;
- ``none`` — скрыть элемент.

Пример:
```css
.block {
  display: block;
  background: #e3f2fd;
  padding: 8px;
}

.inline {
  display: inline;
  background: #fff3e0;
}

.inline-block {
  display: inline-block;
  width: 100px;
  height: 40px;
  background: #e8f5e9;
}

.flex {
  display: flex;
  gap: 10px;
}

.hidden {
  display: none;
}
```
```html
<div class="block">Блочный элемент</div>
<span class="inline">Строчный</span>
<span class="inline">в потоке</span>
<div class="inline-block">inline-block</div>
<div class="flex">
  <div>1</div><div>2</div><div>3</div>
</div>
<p class="hidden">Этот текст не виден</p>
```
#### Способы внедрения стилей
##### 1. Встроенный стиль — атрибут ``style``
Описание: Стили прописываются прямо в атрибуте style тега. Имеют самый высокий приоритет (кроме ``!important``). Подходят для точечного оформления, но плохо масштабируются.

Пример:
```html
<p style="color: red; font-size: 18px;">Красный текст 18px</p>

<div style="background-color: #f0f0f0; padding: 16px; border-radius: 8px;">
  Блок с встроенными стилями
</div>

<button style="background: #3498db; color: white; border: none; padding: 10px 20px;">
  Кнопка
</button>
```
Плюсы: быстро, наглядно.

Минусы: смешивает структуру и оформление, нельзя переиспользовать, сложно поддерживать.

##### 2. Внутренняя таблица стилей — ``<style>...</style>``
Описание: Стили пишутся внутри тега ``<style>`` в ``<head>``. Действуют на всю страницу.

Пример:
```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Внутренние стили</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      margin: 0;
      padding: 20px;
    }

    h1 {
      color: #2c3e50;
      text-align: center;
    }

    .card {
      background: white;
      padding: 16px;
      border: 1px solid #ddd;
      border-radius: 8px;
      max-width: 400px;
      margin: 0 auto;
    }
  </style>
</head>
<body>
  <h1>Заголовок</h1>
  <div class="card">Текст карточки</div>
</body>
</html>
```
Плюсы: все стили в одном файле с HTML, не нужно подключать внешний файл.

Минусы: стили нельзя переиспользовать на других страницах.

##### 3. Внешняя таблица стилей — отдельный файл
Описание: Стили выносятся в отдельный ``.css-файл`` и подключаются через ``<link rel="stylesheet" href="...">.`` Самый правильный и масштабируемый способ.

Структура проекта:
```text
project/
├── index.html
├── about.html
└── css/
    └── styles.css
```
**index.html:**
```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Внешние стили</title>
  <link rel="stylesheet" href="css/styles.css">
</head>
<body>
  <h1>Заголовок</h1>
  <div class="card">Текст карточки</div>
</body>
</html>
```
**css/styles.css:**
```css
body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
  margin: 0;
  padding: 20px;
}

h1 {
  color: #2c3e50;
  text-align: center;
}

.card {
  background: white;
  padding: 16px;
  border: 1px solid #ddd;
  border-radius: 8px;
  max-width: 400px;
  margin: 0 auto;
}
```
Плюсы: переиспользование, кэширование браузером, чистое разделение HTML и CSS, удобно поддерживать.

Минусы: нужен дополнительный запрос к файлу (незначительно).

#### Сравнение способов
Способ	|Где пишется	|Приоритет	|Переиспользование
------- | ------------ | ---------------- | -------------
Встроенный (style)	 |В атрибуте тега	 |Самый высокий	 |Нет
Внутренний (<style>)	 |В <head>	 |Средний	 |Только в пределах страницы
Внешний (<link>)	 |Отдельный .css	 |Обычный	 |Да, на всех страницах

Рекомендуется использовать внешние таблицы стилей как основной способ, а остальные — для точечных правок или быстрых прототипов.

#### Абсолютные и относительные пути
Описание: Путь указывает, где находится подключаемый файл: CSS, картинка, шрифт, другая страница. От правильного пути зависит, найдёт ли браузер ресурс.

##### Абсолютные пути

Начинаются с ``/ (от корня сайта)`` или с полного URL ``(http://, https://)``. Не зависят от расположения текущего файла.

Примеры:

```html
<!-- От корня сайта -->
<link rel="stylesheet" href="/css/styles.css">
<img src="/images/logo.png" alt="Логотип">

<!-- Полный URL -->
<link rel="stylesheet" href="https://cdn.example.com/css/styles.css">
<img src="https://example.com/images/cat.jpg" alt="Кот">
```
Когда использовать: подключение внешних CDN-ресурсов, файлы, которые точно лежат в известном месте от корня.

##### Относительные пути

Считаются от местоположения текущего файла (HTML-документа).

Обозначения:
- ``file.css`` или ``./file.css`` — файл в той же папке;
- ``css/styles.css`` — файл в подпапке css;
- ``../images/cat.jpg`` — подняться на уровень выше и зайти в images;
- ``../../assets/img.png`` — подняться на два уровня выше.

Структура проекта:

```text
project/
├── index.html
├── about/
│   └── team.html
├── css/
│   └── styles.css
└── images/
    └── cat.jpg
```
**index.html** (в корне):
```html
<link rel="stylesheet" href="css/styles.css">
<img src="images/cat.jpg" alt="Кот">
about/team.html (во вложенной папке):

html
<!-- Подняться на уровень выше, затем в css -->
<link rel="stylesheet" href="../css/styles.css">

<!-- Подняться на уровень выше, затем в images -->
<img src="../images/cat.jpg" alt="Кот">

<!-- Ссылка на главную -->
<a href="../index.html">На главную</a>
```
##### Частые ошибки с путями
- Забыли ``../`` — файл ищется не там, где лежит.
- Лишний ``/``в начале относительного пути — превращает его в абсолютный от корня.
- Опечатка в имени файла или папки — регистр важен на Linux-хостингах (Cat.jpg ≠ cat.jpg).
- Пробелы в именах — лучше избегать или использовать %20.
- Неверная вложенность — проверяйте, из какой папки запускается HTML.
- Как проверить: откройте DevTools (F12) → вкладка Network/Сеть → перезагрузите страницу. Если ресурс не загрузился — будет 404, и видно, по какому пути браузер его искал.

##### Итоговая шпаргалка
```css
/* Цвета и фон */
color: #333;
background-color: #f4f4f4;
background-image: url("images/bg.jpg");

/* Текст */
font-size: 16px;
font-style: italic;
font-family: Arial, sans-serif;
text-align: center;
text-transform: uppercase;

/* Рамки и отступы */
border: 1px solid #ddd;
border-color: #2c3e50;
border-radius: 8px;
margin: 0 auto;
padding: 16px;

/* Отображение */
display: block;      /* или inline, inline-block, flex, grid, none */
html
<!-- Внешние стили (лучший способ) -->
<link rel="stylesheet" href="css/styles.css">

<!-- Внутренние стили -->
<style> p { color: red; } </style>

<!-- Встроенные стили -->
<p style="color: red;">Текст</p>
```
