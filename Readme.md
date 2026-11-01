# 🎮 GameVault

**GameVault** — веб-приложение для поиска видеоигр, просмотра информации о них и управления персональной игровой библиотекой.

Данные об играх предоставляются [RAWG Video Games Database API](https://rawg.io/apidocs).

## Технологии

* HTML5 / CSS3
* Vanilla JavaScript (ES6+)
* Fetch API
* LocalStorage
* RAWG REST API

## Функциональность

* Каталог видеоигр с обложками, рейтингами и описаниями.
* Поиск игр по названию.
* Просмотр подробной информации об игре.
* Добавление игр в личную библиотеку.
* Отслеживание статуса прохождения.
* Фильтрация и сортировка игр.

## Структура проекта

```
gamevault/
├── index.html
├── README.md
├── .gitignore
├── assets/
│   └── images/
└── src/
    ├── app.js
    ├── models/
    │   └── Game.js
    ├── services/
    │   └── GameApiService.js
    ├── views/
    │   └── GameView.js
    ├── storage/
    │   └── StorageService.js
    └── styles/
        └── style.css
```

### Основные компоненты

* `<span>Game</span>` — модель данных видеоигры.
* `<span>GameApiService</span>` — HTTP-запросы к RAWG API.
* `<span>GameView</span>` — отображение каталога и карточек игр.
* `<span>StorageService</span>` — работа с LocalStorage.
* `<span>app.js</span>` — инициализация приложения и взаимодействие компонентов.

## Запуск

1. Клонировать репозиторий.
2. Получить API-ключ на [RAWG](https://rawg.io/apidocs).
3. Настроить подключение к API.
4. Запустить локальный HTTP-сервер:

```
python3 -m http.server 8080
```

Открыть `<span>http://localhost:8080</span>`.

> API-ключ нельзя считать секретным при использовании напрямую в браузере. Для публичного развёртывания рекомендуется серверный прокси.

## API

Базовый URL:

```
https://api.rawg.io/api
```

Основные endpoints:


| Метод | Endpoint                          | Описание                       |
| ---------- | --------------------------------- | -------------------------------------- |
| GET        | `<span>/games</span>`             | Получение списка игр |
| GET        | `<span>/games?search=doom</span>` | Поиск игр                      |
| GET        | `<span>/games/{id}</span>`        | Информация об игре     |
| GET        | `<span>/genres</span>`            | Список жанров              |
| GET        | `<span>/platforms</span>`         | Список платформ          |

Для запросов используется параметр `<span>key</span>` с API-ключом.

## Дальнейшее развитие

* Расширенная личная библиотека.
* Управление прогрессом прохождения.
* Backend на PHP.
* REST API и база данных.
* Авторизация пользователей.

---

Game data provided by [RAWG](https://rawg.io/).
