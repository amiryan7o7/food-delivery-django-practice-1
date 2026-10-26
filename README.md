# Вкусно — интернет-магазин доставки еды

Репозиторий: https://github.com/amiryan7o7/food-delivery-django-practice-1

Практическая работа № 1 «Создание первого проекта».

Автор: Амирян Е.Г., ВТ-1-24. Дисциплина: «Разработка кода информационных ресурсов».
Преподаватель: Григоренко Н.И. Дата: 26.10.2026.

## Возможности

- Три страницы: главная `/`, каталог `/catalog/`, «О нас» `/about/`.
- Единый header, навигация с активной страницей и footer.
- Общий базовый шаблон, отдельные представления и маршруты приложения.
- Шесть демонстрационных блюд; фильтрация по категориям и поиск через GET.
- Адаптивная вёрстка; все изображения и CSS включены в проект.

## Запуск на macOS и Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Открыть http://127.0.0.1:8000/ .

## Запуск на Windows PowerShell

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Если активация недоступна, можно запускать Python напрямую:
`.venv\Scripts\python.exe manage.py runserver` после установки зависимостей и миграций.

## Проверка

```bash
python manage.py check
python manage.py test
```

## Структура

`config/` — настройки и основной urls.py; `store/` — одно приложение.
`store/data.py` — демонстрационные данные; `store/views.py` — обработчики;
`store/urls.py` — маршруты; `store/templates/store/` — шаблоны;
`store/static/store/` — стили и оригинальные SVG-иллюстрации.

## Границы практической работы

Проект демонстрирует страницы магазина и маршрутизацию. Оформление заказа,
оплата, корзина и база товаров не входят в задание № 1. Названия блюд и цены учебные.
Настройки предназначены для локального запуска: DEBUG=True. Для публикации нужны
отдельные производственные настройки и значение DJANGO_SECRET_KEY в окружении.
`.env.example` — пример; автоматическое чтение `.env` не используется.

Виртуальное окружение и SQLite не хранятся в Git: они создаются локально командами выше.

## Вид главной страницы

![Главная страница](docs/screenshots/home.png)

Полные скриншоты каталога и страницы «О нас» находятся в `docs/screenshots/`.
Результаты автоматических и браузерных проверок — в `docs/`.

## Публикация на GitHub из архива

После создания пустого репозитория на GitHub выполнить в папке проекта:

```bash
git init -b main
git add .
git commit -m "Create food delivery Django project"
```

Затем добавить URL именно своего репозитория командой `git remote add origin`
и отправить ветку командой `git push -u origin main` после авторизации GitHub.
Виртуальное окружение, база SQLite и локальные настройки исключены через `.gitignore`.
