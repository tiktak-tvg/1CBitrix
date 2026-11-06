### Работа со стилями текста — свойства CSS
#### 1. text-align — выравнивание текста
Описание: Управляет горизонтальным выравниванием текста внутри блочного элемента.

Значения:

``left`` — по левому краю (по умолчанию для большинства языков);

``right`` — по правому краю;

``center`` — по центру;

``justify`` — по всей ширине блока (пробелы растягиваются так, чтобы края текста были ровными).

Пример:

```css
.left    { text-align: left; }
.right   { text-align: right; }
.center  { text-align: center; }
.justify { text-align: justify; }
html
<div class="left">Текст по левому краю</div>
<div class="right">Текст по правому краю</div>
<div class="center">Текст по центру</div>
<div class="justify">Длинный текст, выровненный по всей ширине блока...</div>
```
Замечание: ``text-align: justify`` хорошо выглядит на длинных абзацах. На коротких строках может давать большие пробелы между словами.

#### 2. text-decoration — оформление текста
Описание: Добавляет или убирает декоративные линии у текста.

Значения:

``none`` — без оформления (часто используется для ссылок, чтобы убрать подчёркивание);

``underline`` — подчёркнутый текст;

``overline`` — линия сверху;

``line-through`` — перечёркивание (зачёркивание);

``blink`` — мигание (устарел, современные браузеры не поддерживают).

Пример:

```css
.none        { text-decoration: none; }
.underline   { text-decoration: underline; }
.overline    { text-decoration: overline; }
.line-through { text-decoration: line-through; }
```
```html
<p class="none">Без оформления</p>
<p class="underline">Подчёркнутый текст</p>
<p class="overline">Линия сверху</p>
<p class="line-through">Зачёркнутый текст</p>
<a href="#" class="none">Ссылка без подчёркивания</a>
```
Комбинирование: можно задать несколько декораций сразу:
```css
.multi {
  text-decoration: underline line-through;
}
```
#### 3. text-shadow — тень для букв
Описание: Создаёт тень у текста. Позволяет «оттенить» буквы, добавить объём или цветной акцент.

Синтаксис:

```text
text-shadow: сдвиг-X сдвиг-Y размытие цвет;
сдвиг-X — смещение по горизонтали (2px вправо, -2px влево);

сдвиг-Y — смещение по вертикали;

размытие — необязательно, чем больше, тем мягче тень;

цвет — цвет тени.
```
Пример:
```css
.shadow-1 {
  text-shadow: 2px 2px #666666;
}

.shadow-2 {
  text-shadow: 0 0 8px #3498db;   /* свечение */
}

.shadow-3 {
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3),
               0 0 12px #ffe066;   /* двойная тень */
}
```
```html
<h2 class="shadow-1">Тень 2px 2px</h2>
<h2 class="shadow-2">Светящийся текст</h2>
<h2 class="shadow-3">Двойная тень</h2>
```
Замечание: у ``text-shadow`` есть приоритетное применение — заголовки, кнопки, акцентные надписи. Слишком сильная тень на обычном тексте ухудшает читаемость.

#### 4. ``letter-spacing`` — межбуквенный интервал
Описание: Задаёт расстояние между соседними буквами текста.

Значения:

``normal`` — значение по умолчанию (определяется браузером и шрифтом);

числовое значение — обычно в ``px, em или rem``. Положительное — разрядка, отрицательное — сжатие.

Примечание: значение ``auto для letter-spacing ``в стандарте CSS не предусмотрено; в слайде, скорее всего, опечатка. Для «впихнуть в одну строку» обычно используют ``white-space: nowrap`` или уменьшение ``font-size``.

Пример:

```css
.normal  { letter-spacing: normal; }
.wide    { letter-spacing: 5px; }
.negative { letter-spacing: -1px; }
```
```html
<p class="normal">Обычный межбуквенный интервал</p>
<p class="wide">Р А З Р Я Д К А</p>
<p class="negative">Сжатый интервал</p>
```
Где применять: заголовки, логотипы, короткие надписи. На длинном тексте большая разрядка затрудняет чтение.

#### 5. ``line-height`` — межстрочный интервал
Описание: Задаёт высоту строки — расстояние между строками по вертикали. Сильно влияет на читаемость текста.

Значения:

``normal`` — значение по умолчанию (обычно ~1.2 от размера шрифта);

``число без единиц`` — множитель от размера шрифта (например, 1.5 = 150%);

``число с единицами`` — конкретная высота (24px, 1.5em).

Пример:

```css
.tight {
  line-height: 1;     /* строки почти слипаются */
}

.normal {
  line-height: normal;
}

.comfortable {
  line-height: 1.6;   /* удобно для чтения */
}

.px {
  line-height: 28px;  /* точное значение */
}
```
```html
<p class="tight">Плотный межстрочный интервал...</p>
<p class="comfortable">Комфортный межстрочный интервал...</p>
```
Рекомендация: для основного текста — ```line-height: 1.5–1.7.``` Для заголовков — 1.1–1.3. Это улучшает читаемость.

#### 6. ``word-spacing`` — расстояние между словами
Описание: Задаёт дополнительный интервал между словами. Работает поверх обычного пробела.

Значения:

``normal`` — значение по умолчанию;

``числовое значение с единицами (px, em)`` — добавка к обычному пробелу.

Пример:

```css
.normal { word-spacing: normal; }
.wide   { word-spacing: 10px; }
.tight  { word-spacing: -3px; }
```
```html
<p class="normal">Обычный интервал между словами</p>
<p class="wide">Широкий интервал между словами</p>
<p class="tight">Узкий интервал между словами</p>
```
Где применять: акцентные заголовки, декоративные надписи. Для длинного текста изменение ``word-spacing`` может выглядеть неаккуратно.

#### 7. ``text-transform`` — вид букв (регистр)
Описание: Управляет регистром букв, не меняя сам текст в HTML. Удобно для кнопок, меню, заголовков.

Значения:

``none`` — без изменений;

``capitalize`` — каждое слово с заглавной буквы;

``uppercase`` — ВСЕ БУКВЫ ПРОПИСНЫЕ;

``lowercase`` — все буквы строчные.

Пример:
```css
.none       { text-transform: none; }
.capitalize { text-transform: capitalize; }
.uppercase  { text-transform: uppercase; }
.lowercase  { text-transform: lowercase; }
```
```html
<p class="none">привет мир html и css</p>
<p class="capitalize">привет мир html и css</p>
<p class="uppercase">привет мир html и css</p>
<p class="lowercase">ПРИВЕТ МИР HTML И CSS</p>
```
Важно: в исходном HTML текст остаётся неизменным — меняется только отображение. Если нужно скопировать текст со страницы, скопируется исходный вариант.

Готовая демонстрационная страница ``index.html``:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Стили текста</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 820px;
      margin: 40px auto;
      padding: 0 16px;
      color: #222;
    }

    h1 {
      color: #2c3e50;
      border-bottom: 3px solid #3498db;
      padding-bottom: 8px;
      text-align: center;
    }

    h2 {
      color: #34495e;
      margin-top: 32px;
      font-size: 20px;
    }

    .example {
      background: #f7f9fb;
      border-left: 4px solid #3498db;
      padding: 10px 16px;
      margin: 8px 0;
      border-radius: 4px;
    }

    .box {
      background: #eef2f5;
      padding: 8px 12px;
      margin: 6px 0;
      border-radius: 4px;
    }

    /* text-align */
    .left    { text-align: left; }
    .right   { text-align: right; }
    .center  { text-align: center; }
    .justify { text-align: justify; }

    /* text-decoration */
    .none         { text-decoration: none; }
    .underline    { text-decoration: underline; }
    .overline     { text-decoration: overline; }
    .line-through { text-decoration: line-through; }

    /* text-shadow */
    .shadow-1 { text-shadow: 2px 2px #666666; }
    .shadow-2 { text-shadow: 0 0 8px #3498db; }
    .shadow-3 {
      text-shadow: 1px 1px 2px rgba(0,0,0,.3), 0 0 12px #ffe066;
    }

    /* letter-spacing */
    .ls-normal { letter-spacing: normal; }
    .ls-wide   { letter-spacing: 5px; }
    .ls-neg    { letter-spacing: -1px; }

    /* line-height */
    .lh-tight   { line-height: 1; }
    .lh-normal  { line-height: normal; }
    .lh-forest  { line-height: 1.6; }

    /* word-spacing */
    .ws-normal { word-spacing: normal; }
    .ws-wide   { word-spacing: 10px; }
    .ws-tight  { word-spacing: -3px; }

    /* text-transform */
    .tt-capitalize { text-transform: capitalize; }
    .tt-upper      { text-transform: uppercase; }
    .tt-lower      { text-transform: lowercase; }
  </style>
</head>
<body>

  <h1>Стили текста</h1>

  <!-- text-align -->
  <h2>text-align</h2>
  <div class="box left">Текст по левому краю</div>
  <div class="box right">Текст по правому краю</div>
  <div class="box center">Текст по центру</div>
  <div class="box justify">
    Длинный текст, выровненный по всей ширине блока. Пробелы
    растягиваются так, чтобы правый край тоже был ровным. Хорошо работает
    на длинных абзацах.
  </div>

  <!-- text-decoration -->
  <h2>text-decoration</h2>
  <p class="box none">Без оформления</p>
  <p class="box underline">Подчёркнутый текст</p>
  <p class="box overline">Линия сверху</p>
  <p class="box line-through">Зачёркнутый текст</p>
  <p class="box"><a href="#" class="none">Ссылка без подчёркивания</a></p>

  <!-- text-shadow -->
  <h2>text-shadow</h2>
  <p class="box shadow-1">Тень 2px 2px</p>
  <p class="box shadow-2">Светящийся текст</p>
  <p class="box shadow-3">Двойная тень</p>

  <!-- letter-spacing -->
  <h2>letter-spacing</h2>
  <p class="box ls-normal">Обычный межбуквенный интервал</p>
  <p class="box ls-wide">РАЗРЯДКА</p>
  <p class="box ls-neg">Сжатый интервал</p>

  <!-- line-height -->
  <h2>line-height</h2>
  <p class="box lh-tight">
    Плотный межстрочный интервал. Строки почти слипаются,
    читать неудобно. Используется редко, например для компактных
    подписей.
  </p>
  <p class="box lh-forest">
    Комфортный межстрочный интервал. Строки дышат, читать легко.
    Значение 1.5–1.7 считается стандартом для основного текста.
  </p>

  <!-- word-spacing -->
  <h2>word-spacing</h2>
  <p class="box ws-normal">Обычный интервал между словами</p>
  <p class="box ws-wide">Широкий интервал между словами</p>
  <p class="box ws-tight">Узкий интервал между словами</p>

  <!-- text-transform -->
  <h2>text-transform</h2>
  <p class="box">Без изменений: привет мир html и css</p>
  <p class="box tt-capitalize">capitalize: привет мир html и css</p>
  <p class="box tt-upper">uppercase: привет мир html и css</p>
  <p class="box tt-lower">lowercase: ПРИВЕТ МИР HTML И CSS</p>

</body>
</html>
```
#### Итоговая шпаргалка
```css
/* Выравнивание */
text-align: left | right | center | justify;

/* Оформление */
text-decoration: none | underline | overline | line-through;

/* Тень */
text-shadow: 2px 2px #666;
text-shadow: 0 0 8px #3498db;

/* Межбуквенный интервал */
letter-spacing: normal | 5px | -1px;

/* Межстрочный интервал */
line-height: normal | 1.5 | 24px;

/* Интервал между словами */
word-spacing: normal | 10px;

/* Регистр */
text-transform: none | capitalize | uppercase | lowercase;
```
Практические советы:
```txt
line-height: 1.5–1.7 — для читаемого текста.

text-align: center — для заголовков, justify — для длинных абзацев.

text-decoration: none — почти всегда для ссылок, если их вид оформлен иначе (например, цветом и фоном).

text-transform: uppercase — удобно для кнопок и меню, но не для длинного текста.

text-shadow — аккуратно: сильная тень ухудшает читаемость.

letter-spacing и word-spacing — для акцентных коротких надписей, не для абзацев.
```
