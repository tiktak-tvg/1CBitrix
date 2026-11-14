### Семантика HTML5. 
В новой версии HTML5 были введены так называемые семантические элементы, которые  четко описывают, что они означают, как браузеру, так и веб-разработчику. То есть теперь, указывая, например, теги ``<header>`` браузер и веб-разработчик точно понимают, что работа ведется в заголовке страницы. 

Продолжим изучение семантики HTML5. В прошлом (до HTML5) разработчики использовали для всего тег ``<div>`` с разными классами (например, ``<div class="header">, <div class="footer">``). Браузер понимал, что это просто блок, но не понимал его смысла.

Семантические теги решили эту проблему. Вот основные из них:

#### Новые теги семантики HTML5:
- ``<header>`` — Шапка страницы или отдельного раздела. Обычно содержит логотип, название сайта, главное меню.

- ``<nav>`` — Навигация. Блок с основными ссылками для перемещения по сайту (меню).

- ``<main>`` — Основное содержимое страницы. Должен быть только один на странице и не включать в себя шапку и подвал.

- ``<section>`` — Смысловой раздел страницы. Обычно содержит заголовок и объединяет контент по одной теме.

- ``<article>`` — Независимая, целостная единица контента (статья в блоге, пост в соцсети, карточка товара). Ее можно вырвать из контекста страницы, и она сохранит смысл.

- ``<aside>`` — Боковая панель (сайдбар) или врезка. Содержит информацию, косвенно связанную с основным контентом (реклама, список последних новостей, автор статьи).

- ``<footer>`` — Подвал страницы или раздела. Содержит копирайт, контактные данные, ссылки на соцсети.

- ``<figure>`` и ``<figcaption>`` — Используются для иллюстраций. ``<figure>`` оборачивает картинку, схему или код, а ``<figcaption>`` добавляет к ней подпись.

- ``<details>`` и ``<summary>`` — Интерактивный виджет (как спойлер). ``<summary>`` — это видимая часть (заголовок), при клике на которую раскрывается содержимое ``<details>``.

- ``<time>`` — Указывает дату или время в машиночитаемом формате (важно для поисковиков, чтобы они понимали, когда была написана статья).

#### Сравнение: Было (HTML4) vs Стало (HTML5)

#### Старый подход (набор ``<div>``):
```html
<div class="header">
  <div class="logo">Мой сайт</div>
  <div class="menu">...</div>
</div>
<div class="content">
  <div class="post">...</div>
</div>
<div class="footer">...</div>
```
В этом коде много скобок и классов, скринридеры (программы для незрячих) не поймут, где меню, а поисковики хуже индексируют страницу.

#### Современный подход (Семантика HTML5):

```html
<header>
  <h1>Мой сайт</h1>
  <nav>...</nav>
</header>
<main>
  <article>...</article>
</main>
<footer>...</footer>
```
Код читается как обычный текст. Браузер, поисковики и другие разработчики сразу видят структуру страницы.

#### Пример полной структуры страницы

Давайте соберем полноценный каркас типичной веб-страницы (например, блога), используя семантические теги, и немного оформим их через CSS, чтобы вы наглядно увидели, где какой блок находится.
```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Семантика HTML5</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 900px;
      margin: 20px auto;
      padding: 0 15px;
      color: #333;
    }

    /* Оформляем семантические теги как блоки для наглядности */
    header, nav, main, footer, section, article, aside {
      border-radius: 6px;
      margin-bottom: 10px;
      padding: 15px;
    }

    header { background-color: #2c3e50; color: white; }
    nav { background-color: #34495e; text-align: center; }
    nav a { color: white; margin: 0 10px; text-decoration: none; }
    
    main { 
      display: flex; /* Ставим контент и сайдбар в один ряд */
      gap: 15px; 
      background-color: #ecf0f1; 
      padding: 0;
      border: none;
    }
    
    .content-area { flex: 2; } /* Основная часть шире */
    .sidebar-area { flex: 1; } /* Сайдбар уже */

    section { background-color: white; }
    article { background-color: #f9f9f9; border-left: 4px solid #3498db; }
    aside { background-color: #e8f4f8; }
    footer { background-color: #2c3e50; color: white; text-align: center; }
  </style>
</head>
<body>

  <!-- ШАПКА САЙТА -->
  <header>
    <h1>Блог веб-разработчика</h1>
    <p>Учим HTML и CSS вместе</p>
  </header>

  <!-- НАВИГАЦИЯ -->
  <nav>
    <a href="#">Главная</a>
    <a href="#">Статьи</a>
    <a href="#">Обо мне</a>
  </nav>

  <!-- ОСНОВНОЙ КОНТЕНТ (состоит из контента и сайдбара) -->
  <main>
    
    <!-- Основная зона -->
    <div class="content-area">
      <!-- Смысловой раздел -->
      <section>
        <h2>Последние записи</h2>
        
        <!-- Независимая статья -->
        <article>
          <h3>Что такое семантика?</h3>
          <p>Семантика — это использование тегов по их прямому назначению.</p>
          <time datetime="2024-05-20">20 мая 2024</time>
        </article>

        <article>
          <h3>Как работает CSS?</h3>
          <p>CSS отвечает за внешний вид наших HTML-страниц.</p>
          <time datetime="2024-05-18">18 мая 2024</time>
        </article>

      </section>
    </div>

    <!-- Боковая панель -->
    <div class="sidebar-area">
      <aside>
        <h3>Об авторе</h3>
        <p>Привет! Меня зовут Иван, я изучаю фронтенд.</p>
      </aside>
      
      <aside>
        <h3>Реклама</h3>
        <p>Здесь могла быть ваша реклама.</p>
      </aside>
    </div>

  </main>

  <!-- ПОДВАЛ -->
  <footer>
    <p>&copy; 2024 Блог веб-разработчика. Все права защищены.</p>
  </footer>

</body>
</html>
```

<img width="964" height="739" alt="image" src="https://github.com/user-attachments/assets/7850ed53-b9be-40ad-991e-407b6302902d" />

#### В чем главные плюсы семантики?
SEO (Поисковики): Google и Яндекс лучше понимают, где находится главный текст статьи, а где рекламный сайдбар, поэтому сайт может выше ранжироваться.

Доступность (Accessibility): Слепые пользователи используют программы-скринридеры. Они могут нажать горячую клавишу и сразу перейти к тегу ``<main>``, пропустив надоедливое меню.

Читаемость кода: Разработчику не нужно всматриваться в классы ``<div class="main-content">``, он сразу видит тег ``<main>``.

Пример семантики

#### 1. HTML-код (index.html)
Здесь мы используем теги по их прямому смыслу. Обратите внимание, что тег <nav> находится внутри <header>, так как навигация — это часть шапки сайта.

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Семантическая разметка</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="layout-wrapper">
    
    <!-- ШАПКА (Содержит текст и навигацию) -->
    <header>
      <div class="header-text">HEADER</div>
      <nav>NAV</nav>
    </header>

    <!-- ОСНОВНОЙ КОНТЕНТ -->
    <main>
      <div class="main-title">MAIN</div>
      <div class="sections-container">
        <section>SECTION</section>
        <section>SECTION</section>
      </div>
    </main>

    <!-- ПОДВАЛ -->
    <footer>FOOTER</footer>

  </div>

</body>
</html>
```
#### 2. CSS-код (style.css)
Чтобы расставить блоки именно так, как на картинке, мы используем display: flex.
```css
/* Сброс базовых отступов для удобства */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  padding: 20px;
  background-color: #f4f4f4;
}

/* Обертка для всего макета, чтобы задать отступы между блоками */
.layout-wrapper {
  max-width: 800px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 10px; /* Расстояние между Header, Main и Footer */
}

/* ================= HEADER ================= */
header {
  border: 2px solid #3b82f6; /* Синяя рамка */
  display: flex;
  padding: 15px;
  align-items: center;
}

.header-text {
  flex: 1; /* Занимает 1/3 ширины */
  text-align: center;
  font-weight: bold;
}

nav {
  flex: 2; /* Занимает 2/3 ширины */
  border: 2px solid #eab308; /* Желтая рамка */
  padding: 20px;
  text-align: center;
  font-weight: bold;
}

/* ================= MAIN ================= */
main {
  border: 2px solid #10b981; /* Зеленая рамка */
  padding: 15px;
}

.main-title {
  text-align: center;
  font-weight: bold;
  margin-bottom: 30px;
  margin-top: 10px;
}

/* Контейнер для секций (Flexbox ставит их в один ряд) */
.sections-container {
  display: flex;
  justify-content: center;
  gap: 50px; /* Расстояние между двумя SECTION */
  margin-bottom: 10px;
}

section {
  border: 2px solid #f97316; /* Оранжевая рамка */
  width: 250px;
  height: 150px;
  display: flex;
  align-items: center; /* Центрируем текст по вертикали */
  justify-content: center; /* Центрируем текст по горизонтали */
  font-weight: bold;
}

/* ================= FOOTER ================= */
footer {
  border: 2px solid #3b82f6; /* Синяя рамка */
  padding: 25px;
  text-align: center;
  font-weight: bold;
}
```

<img width="874" height="480" alt="image" src="https://github.com/user-attachments/assets/baa9fb9a-d8a3-4353-8b6e-5fd970fe3294" />

##### Вот готовый пример, который в точности повторяет дизайн со скриншота. 
Я использовал семантические теги ``(<header>, <nav>, <main>, <article>, <aside>, <footer>)`` и CSS-технологию Flexbox для создания двух колонок (основной контент и боковая панель).

Сохраните этот код в файл index.html и откройте в браузере.

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Блог веб-разработчика</title>
  <style>
    /* --- БАЗОВЫЕ СТИЛИ --- */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; /* Похожий шрифт */
      background-color: #e8ebf0; /* Светло-серый фон страницы */
      color: #333;
      line-height: 1.6;
      padding: 20px;
    }

    /* Общий контейнер, центрирующий контент */
    .container {
      max-width: 960px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 15px; /* Отступы между крупными блоками */
    }

    /* Общие стили для темных блоков (шапка, меню, подвал) */
    .dark-block {
      background-color: #2c3e50; /* Темно-синий цвет */
      color: white;
      border-radius: 8px;
    }

    /* --- ШАПКА --- */
    header {
      padding: 30px;
    }

    header h1 {
      font-size: 28px;
      margin-bottom: 10px;
      font-weight: 600;
    }

    header p {
      font-size: 16px;
      color: #d1d8e0;
    }

    /* --- НАВИГАЦИЯ --- */
    nav {
      padding: 15px 30px;
      display: flex;
      justify-content: center; /* Центрируем ссылки */
      gap: 30px; /* Расстояние между ссылками */
    }

    nav a {
      color: white;
      text-decoration: none;
      font-size: 16px;
      transition: opacity 0.2s;
    }

    nav a:hover {
      opacity: 0.7;
    }

    /* --- ОСНОВНОЙ КОНТЕНТ (Flexbox для двух колонок) --- */
    main {
      display: flex;
      gap: 20px;
      align-items: flex-start; /* Колонки не растягиваются по высоте без нужды */
    }

    /* Левая колонка (Контент) */
    .content-area {
      flex: 2.5; /* Занимает больше места */
      background-color: white;
      border-radius: 8px;
      padding: 30px;
    }

    .content-area h2 {
      font-size: 22px;
      margin-bottom: 20px;
      color: #2c3e50;
    }

    /* Карточка статьи */
    article {
      background-color: #f8f9fa;
      padding: 20px;
      border-radius: 6px;
      margin-bottom: 15px;
      border-left: 4px solid #3498db; /* Синяя полоса слева */
      box-shadow: 0 2px 5px rgba(0,0,0,0.02); /* Легкая тень */
    }

    article h3 {
      font-size: 18px;
      margin-bottom: 10px;
      color: #2c3e50;
    }

    article p {
      font-size: 15px;
      margin-bottom: 15px;
      color: #555;
    }

    article time {
      font-size: 13px;
      color: #888;
    }

    /* Правая колонка (Сайдбар) */
    .sidebar-area {
      flex: 1; /* Занимает меньше места */
      background-color: #f0f6f9; /* Светло-голубой фон */
      border-radius: 8px;
      padding: 25px;
    }

    .widget {
      margin-bottom: 30px;
    }

    .widget:last-child {
      margin-bottom: 0;
    }

    .widget h3 {
      font-size: 18px;
      margin-bottom: 10px;
      color: #2c3e50;
    }

    .widget p {
      font-size: 15px;
      color: #555;
    }

    /* --- ПОДВАЛ --- */
    footer {
      padding: 20px;
      text-align: center;
      font-size: 15px;
    }

    /* Адаптивность для мобильных телефонов (чтобы колонки вставали друг под друга) */
    @media (max-width: 768px) {
      main {
        flex-direction: column;
      }
      .content-area, .sidebar-area {
        flex: none;
        width: 100%;
      }
    }
  </style>
</head>
<body>

  <div class="container">

    <!-- СЕМАНТИЧЕСКАЯ ШАПКА -->
    <header class="dark-block">
      <h1>Блог веб-разработчика</h1>
      <p>Учим HTML и CSS вместе</p>
    </header>

    <!-- СЕМАНТИЧЕСКАЯ НАВИГАЦИЯ -->
    <nav class="dark-block">
      <a href="#">Главная</a>
      <a href="#">Статьи</a>
      <a href="#">Обо мне</a>
    </nav>

    <!-- СЕМАНТИЧЕСКИЙ ОСНОВНОЙ КОНТЕНТ -->
    <main>
      
      <!-- Левая колонка -->
      <section class="content-area">
        <h2>Последние записи</h2>
        
        <article>
          <h3>Что такое семантика?</h3>
          <p>Семантика — это использование тегов по их прямому назначению.</p>
          <time datetime="2024-05-20">20 мая 2024</time>
        </article>

        <article>
          <h3>Как работает CSS?</h3>
          <p>CSS отвечает за внешний вид наших HTML-страниц.</p>
          <time datetime="2024-05-18">18 мая 2024</time>
        </article>
      </section>

      <!-- Правая колонка -->
      <aside class="sidebar-area">
        <div class="widget">
          <h3>Об авторе</h3>
          <p>Привет! Меня зовут Иван, я изучаю фронтенд.</p>
        </div>
        
        <div class="widget">
          <h3>Реклама</h3>
          <p>Здесь могла быть ваша реклама.</p>
        </div>
      </aside>

    </main>

    <!-- СЕМАНТИЧЕСКИЙ ПОДВАЛ -->
    <footer class="dark-block">
      <p>&copy; 2024 Блог веб-разработчика. Все права защищены.</p>
    </footer>

  </div>

</body>
</html>
```

<img width="974" height="749" alt="image" src="https://github.com/user-attachments/assets/07966c08-8526-461a-afbb-45b70d2d7adc" />
