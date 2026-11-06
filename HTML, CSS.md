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
