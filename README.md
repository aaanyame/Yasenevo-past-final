
Документация проекта «Бизнес-квартал "Ясенево"»

📌 Описание проекта

Проект представляет собой многостраничный сайт бизнес-квартала «Ясенево», сверстанный с использованием HTML, CSS и SCSS. В проекте используются современные подходы, такие как адаптивная вёрстка и модульная структура стилей.

🗂️ Структура папок проекта

Q:/Anna/Yasenevo past final/
│
├── 📄 index.html        (Главная страница)
├── 📄 location.html     (Страница «Расположение» - для вашей дальнейшей доработки)
├── 📄 plans.html        (Страница «Планировки» - для вашей дальнейшей доработки)
│
├── 📁 .vscode/          (Настройки среды VS Code)
│
├── 📁 assets/
│   ├── 📁 files/        (Файлы для скачивания, презентации)
│   ├── 📁 fonts/        (Файлы шрифтов Montserrat)
│   └── 📁 images/       (Изображения сайта в форматах PNG и WebP)
│
├── 📁 css/              (Минифицированные стили, автоматически генерируются из SCSS)
│   ├── about.min.css
│   ├── fonts.min.css
│   ├── footer.min.css
│   ├── header.min.css
│   ├── hero.min.css
│   ├── inf.min.css
│   ├── main.min.css
│   ├── map.min.css
│   ├── pdf.min.css
│   ├── picture.min.css
│   ├── reset.min.css
│   └── style.min.css (главный CSS-файл, подключаемый к HTML)
│
└── 📁 scss/             (Исходные файлы SCSS)
    ├── fonts.scss      (Подключение шрифтов)
    ├── main.scss       (Основные стили и переменные)
    ├── reset.scss      (Сброс базовых стилей браузеров)
    ├── style.scss      (Главный SCSS-файл, который собирает все стили воедино)
    └── 📁 blocks/      (SCSS-стили для отдельных секций и компонентов)
        ├── about.scss
        ├── footer.scss
        ├── header.scss
        ├── hero.scss
        ├── inf.scss
        ├── map.scss
        ├── pdf.scss
        └── picture.scss

📚 Работа с проектом 

1. Установка и подготовка:

Убедитесь, что у вас установлен VS Code с расширениями:

Live Server (для запуска HTML)

Live Sass Compiler (для компиляции SCSS в CSS)

2️. Запуск проекта:

Откройте проект в VS Code.

Откройте файл index.html и нажмите Go Live (в правом нижнем углу).

Сайт откроется в браузере по адресу http://127.0.0.1:5500/.

3️. Работа с SCSS:

В папке scss/blocks/ создавайте файлы для своих страниц к примеру ( hero-plans.scss, hero-location.scss, plans.scss).

Подключите созданные файлы в главный SCSS-файл style.scss командой:

@import url('./hero-location.min.css');
@import url('./hero-plans.min.css');
@import url('./plans.min.css');

Файлы будут автоматически компилироваться в папку css/ при сохранении.

4️. Подключение CSS в HTML:

В свои HTML-файлы подключайте только главный CSS-файл: (уже подключен)

<link rel="stylesheet" href="css/style.min.css">

⚙️ Важные примечания:

Не редактируйте файлы в папке css/ напрямую. Все изменения только через файлы в папке scss/.

Используйте комментарии и осмысленные имена классов, чтобы улучшить читаемость и понимание вашего кода.

Для просмотра всех изменений используйте Live Server и Live Sass Compiler.

📝 Комментарии по коду

Комментарии и пояснения по логике стилей добавляйте только в SCSS-файлах, чтобы не потерять их при компиляции.

Пример комментария:

// Этот блок регулирует стиль кнопки скачивания
.btn-download {
  padding: 10px 20px;
  background-color: blue;
}

Конфигурация Live Sass Compiler: (уже прописан в папке .vscode в директории проекта)

{
  "liveSassCompile.settings.formats": [
    {
      "format": "compressed",
      "extensionName": ".min.css",
      "savePath": "css"
    }
  ],
  "liveSassCompile.settings.savePathReplacementPairs": [
    {
      "replacePart": "scss",
      "withPart": "css"
    }
  ],
  "liveSassCompile.settings.includeItems": [
    "scss/**/*.scss"
  ],
  "liveSassCompile.settings.excludeList": [
    "**/node_modules/**",
    ".vscode/**"
  ],
  "liveSassCompile.settings.generateMap": true,
  "liveSassCompile.settings.useNewCompiler": true,
  "liveSassCompile.settings.showOutputWindowOn": "Error"
}



