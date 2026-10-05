<p align="center">
  <img src=".github/assets/banner.svg" width="100%" alt="Yatube · Формы" />
</p>

# Yatube · Формы

Создание и редактирование публикаций через веб-интерфейс.

**Учебный проект** · Python · Django 2.2.6 · SQLite · pytest-django  
[Русский](#about) · [English](#english) · [Профиль](https://github.com/artemleonich)

<a id="about"></a>

## О проекте

Учебный этап проекта Yatube из курса бэкенд-разработки на Python [Яндекс Практикума](https://practicum.yandex.ru/). Фокус — ModelForm, обработка запросов и права автора.

- Регистрация, вход и выход пользователя.
- Создание текстовой публикации с необязательной группой.
- Редактирование публикации её автором.
- Профили авторов и страницы отдельных записей.
- Ленты на главной, в группе и в профиле с пагинацией по десять записей.

Это этап текстовых публикаций. Набор тестов Django для моделей, маршрутов, представлений и форм представлен в [hw04_tests](https://github.com/artemleonich/hw04_tests).

## Запуск

```bash
git clone https://github.com/artemleonich/hw03_forms.git
cd hw03_forms
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python yatube/manage.py migrate
python yatube/manage.py createsuperuser
python yatube/manage.py runserver
```

В Windows PowerShell: `.venv\Scripts\Activate.ps1`.

Откройте [127.0.0.1:8000](http://127.0.0.1:8000/). Учётная запись суперпользователя нужна для [админ-панели](http://127.0.0.1:8000/admin/), где можно добавить группы.

## Проверка

Учебные проверки находятся в `tests/`; `pytest.ini` задаёт путь к Django-проекту.

```bash
python -m pytest
```

## Навигация по коду

| Путь | Назначение |
| --- | --- |
| [yatube/posts/](yatube/posts/) | Модели, формы и представления |
| [yatube/templates/](yatube/templates/) | Шаблоны интерфейса |
| [yatube/yatube/settings.py](yatube/yatube/settings.py) | Настройки и SQLite |
| [tests/](tests/) | Учебные проверки |

Зависимости сохранены в учебных версиях из [requirements.txt](requirements.txt). Запуск на новых версиях Python может потребовать адаптации окружения.

<a id="english"></a>

<details>
<summary>English overview</summary>

A Yandex Practicum learning stage focused on Django ModelForm, request handling and author permissions. Users can register, create text posts, choose a group and edit their own posts. Home, group and profile feeds are paginated. The [hw04_tests](https://github.com/artemleonich/hw04_tests) stage adds Django test cases.

Install `requirements.txt` in a virtual environment, run `python yatube/manage.py migrate`, optionally create an admin account with `python yatube/manage.py createsuperuser`, and start `python yatube/manage.py runserver`. Run `python -m pytest` from the repository root. Dependencies are pinned to the original learning versions.

</details>

---

Автор: [Артём Леонов](https://github.com/artemleonich).

