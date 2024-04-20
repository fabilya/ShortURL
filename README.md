## ShortURL - cервис сокращения ссылок

### О проекте:

<b>Проект ShortURL</b> — это инструмент, который позволяет сокращать длинные URL-адреса до более коротких и более управляемых версий. Когда вы вводите длинную ссылку в сервис укорачивания ссылок, он генерирует для нее уникальный короткий URL, который затем можно использовать вместо исходного длинного URL.

### Ключевые возможности сервиса:

- генерация коротких ссылок и связь их с исходными длинными ссылками,
- переадресация на исходный адрес при обращении к коротким ссылкам.

Также доступен API проекта

<details><summary><b>Примеры запросов к API</b></summary>

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



## Инструкции по установке

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:fabilya/yacut.git
cd yacut
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

* Если у вас Linux/macOS

    ```
    source venv/bin/activate
    ```

* Если у вас windows

    ```
    source venv/scripts/activate
    ```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Пример .env-файла который должен быть создан в папке:
```
FLASK_APP=yacut
FLASK_ENV=development
DATABASE_URI=sqlite:///db.sqlite3
SECRET_KEY=MY_SECRET_KEY
```

Автор проекта:
Фабиянский Илья
