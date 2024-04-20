<img src="https://github.com/fabilya/yacut/blob/master/yacut/static/img/logo.png?raw=true" align="right" height="60" />

# ShortURL - cервис сокращения ссылок

## Содержание:
- [О проекте](#о-проекте)
- [Ключевые возможности](#ключевые-возможности-сервиса)
  - [API проекта](#api-проекта)
- [Технологии](#используемые-технологии)
- [Инструкции по установке](#инструкции-по-установке)
- [Авторы](#автор-проекта)

### О проекте:

<b>Проект ShortURL</b> — это инструмент, который позволяет сокращать длинные URL-адреса до более коротких и более управляемых версий. Когда вы вводите длинную ссылку в сервис укорачивания ссылок, он генерирует для нее уникальный короткий URL, который затем можно использовать вместо исходного длинного URL.

### Ключевые возможности сервиса:

- генерация коротких ссылок и связь их с исходными длинными ссылками,
- переадресация на исходный адрес при обращении к коротким ссылкам.

### API проекта

<details><summary>Примеры запросов к API</summary>

- Генерация короткой ссылки: 
    ```SQL
  POST /api/id/
    {
      'url': 'string',
      'custom_id': 'string'
    }
    ```

- Получение оригинальной ссылки по указанному короткому идентификатору:
    ```SQL
    GET /api/id/{short_id}/
    ```
</details>


### Используемые технологии:

- `Python 3.9`
- `Flask 2.0.2`
- `SQLAlchemy 1.4.29`
- `REST API`
- `Jinja2 3.0.3`



### Инструкции по установке
Клонировать репозиторий и перейти в него в командной строке:
```GitBash
git clone git@github.com:fabilya/yacut.git
cd yacut
```

Cоздать и активировать виртуальное окружение:
```Bash
python -m venv venv
```

* Linux/macOS
    ```Bash
    source venv/bin/activate
    ```

* Windows
    ```Bash
    source venv/scripts/activate
    ```

Установить зависимости из файла requirements.txt:
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Пример .env-файла который должен быть создан в корневой папке:
```dotenv
FLASK_APP=yacut
FLASK_ENV=development
DATABASE_URI=sqlite:///db.sqlite3
SECRET_KEY=MY_SECRET_KEY
```

### Создание БД и применение миграции:
```Bash
flask db init
flask db migrate -m "some comment by migrate"
flask db upgrade
```

### Запуск приложения:
```flask run```

### Автор проекта:
[Фабиянский Илья](https://github.com/fabilya)
