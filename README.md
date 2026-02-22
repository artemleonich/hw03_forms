# 📝 Yatube — Forms & Post Management

![Python](https://img.shields.io/badge/Python-3.7-blue?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-2.2-green?logo=django&logoColor=white)

[🇬🇧 English](#english) | [🇷🇺 Русский](#russian)

---

## English

### Overview

Yatube is a social blogging platform built with Django. This iteration (hw03_forms) introduces **form handling** for creating and editing posts. Authenticated users can publish new posts, assign them to thematic groups, and edit their own content through a clean web interface.

### Features

**Content Management**
- Create new posts with text and optional group assignment
- Edit existing posts (author-only access)
- Automatic author assignment on post creation

**Navigation & Display**
- Paginated feed of all posts (10 per page)
- Group-filtered post listings
- User profile pages with post count
- Individual post detail pages

**Authentication & Security**
- Login-required protection for create and edit views
- Author-only editing permissions
- Django’s built-in CSRF protection

### Project Structure

```
hw03_forms/
├── yatube/
│   ├── about/              # Static pages (about, tech)
│   ├── core/               # Shared utilities & context processors
│   ├── posts/              # Main app
│   │   ├── forms.py        # PostForm (ModelForm)
│   │   ├── models.py       # Group, Post models
│   │   ├── views.py        # All view functions
│   │   ├── urls.py         # URL routing
│   │   ├── admin.py        # Admin configuration
│   │   └── tests.py        # Unit tests
│   ├── static/             # CSS, JS, images
│   ├── templates/          # HTML templates
│   ├── users/              # User auth & registration
│   ├── yatube/             # Project settings
│   └── manage.py
├── tests/                  # External test suite
├── requirements.txt
└── setup.cfg
```

### Getting Started

**Prerequisites:** Python 3.7+

1. Clone the repository and navigate into it:
```bash
git clone https://github.com/artemleonich/hw03_forms.git
cd hw03_forms
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
# venv\Scripts\activate  # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Apply migrations and run the server:
```bash
cd yatube
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000/`.

### URL Endpoints

| Endpoint | Description |
|---|---|
| `/` | Main feed with all posts |
| `/group/<slug>/` | Posts filtered by group |
| `/profile/<username>/` | User profile with their posts |
| `/posts/<id>/` | Individual post detail |
| `/create/` | New post form (auth required) |
| `/posts/<id>/edit/` | Edit post form (author only) |

### Tech Stack

Python, Django 2.2, Django Debug Toolbar, pytest, Beautiful Soup 4, sorl-thumbnail

---

## Русский

### Обзор

Yatube — социальная платформа для блогов на Django. Эта итерация (hw03_forms) добавляет **работу с формами** для создания и редактирования постов. Авторизованные пользователи могут публиковать новые записи, привязывать их к тематическим группам и редактировать свои публикации через удобный веб-интерфейс.

### Возможности

**Управление контентом**
- Создание новых постов с текстом и опциональной привязкой к группе
- Редактирование существующих постов (только автор)
- Автоматическое присвоение авторства при создании поста

**Навигация и отображение**
- Пагинация ленты постов (10 на страницу)
- Фильтрация постов по группам
- Профили пользователей со счётчиком публикаций
- Страницы отдельных постов

**Аутентификация и безопасность**
- Защита создания и редактирования через авторизацию
- Права редактирования только для автора
- CSRF-защита Django

### Структура проекта

```
hw03_forms/
├── yatube/
│   ├── about/              # Статические страницы (о проекте, технологии)
│   ├── core/               # Общие утилиты и контекстные процессоры
│   ├── posts/              # Основное приложение
│   │   ├── forms.py        # PostForm (ModelForm)
│   │   ├── models.py       # Модели Group, Post
│   │   ├── views.py        # Функции представлений
│   │   ├── urls.py         # Маршрутизация URL
│   │   ├── admin.py        # Настройка админки
│   │   └── tests.py        # Тесты
│   ├── static/             # CSS, JS, изображения
│   ├── templates/          # HTML-шаблоны
│   ├── users/              # Авторизация и регистрация
│   ├── yatube/             # Настройки проекта
│   └── manage.py
├── tests/                  # Внешние тесты
├── requirements.txt
└── setup.cfg
```

### Быстрый старт

**Требования:** Python 3.7+

1. Клонируйте репозиторий и перейдите в папку:
```bash
git clone https://github.com/artemleonich/hw03_forms.git
cd hw03_forms
```

2. Создайте и активируйте виртуальное окружение:
```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
# venv\Scripts\activate  # Windows
```

3. Установите зависимости:
```bash
pip install -r requirements.txt
```

4. Примените миграции и запустите сервер:
```bash
cd yatube
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Приложение будет доступно по адресу `http://127.0.0.1:8000/`.

### Эндпоинты

| Эндпоинт | Описание |
|---|---|
| `/` | Главная лента всех постов |
| `/group/<slug>/` | Посты, отфильтрованные по группе |
| `/profile/<username>/` | Профиль пользователя с его постами |
| `/posts/<id>/` | Страница отдельного поста |
| `/create/` | Форма создания поста (нужна авторизация) |
| `/posts/<id>/edit/` | Форма редактирования (только автор) |

### Технологии

Python, Django 2.2, Django Debug Toolbar, pytest, Beautiful Soup 4, sorl-thumbnail
