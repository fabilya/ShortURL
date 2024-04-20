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
* Клонировать репозиторий и перейти в него в командной строке:
```GitBash
git clone git@github.com:fabilya/yacut.git
cd yacut
```

* Cоздать виртуальное окружение:
```Bash
python -m venv venv
```
* Активировать виртуальное окружение
<details><summary>Linux/macOS</summary>

```Bash
source venv/bin/activate
```
</details>
<details><summary>Windows</summary>

```Bash
source venv/scripts/activate
```
</details>

* Установить зависимости из файла requirements.txt:
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```

* Пример .env-файла который должен быть создан в корневой папке:
```dotenv
FLASK_APP=yacut
FLASK_ENV=development
DATABASE_URI=sqlite:///db.sqlite3
SECRET_KEY=MY_SECRET_KEY
```

* Создание БД и применение миграции:
```Bash
flask db init
flask db migrate -m "some comment by migrate"
flask db upgrade
```

* Запуск приложения:
```Bash
flask run
```

### Автор проекта:
[Фабиянский Илья](https://github.com/fabilya)
<svg height="32" aria-hidden="true" viewBox="0 0 16 16" version="1.1" width="32" data-view-component="true" class="octicon octicon-mark-github v-align-middle color-fg-default">
    <path d="M8 0c4.42 0 8 3.58 8 8a8.013 8.013 0 0 1-5.45 7.59c-.4.08-.55-.17-.55-.38 0-.27.01-1.13.01-2.2 0-.75-.25-1.23-.54-1.48 1.78-.2 3.65-.88 3.65-3.95 0-.88-.31-1.59-.82-2.15.08-.2.36-1.02-.08-2.12 0 0-.67-.22-2.2.82-.64-.18-1.32-.27-2-.27-.68 0-1.36.09-2 .27-1.53-1.03-2.2-.82-2.2-.82-.44 1.1-.16 1.92-.08 2.12-.51.56-.82 1.28-.82 2.15 0 3.06 1.86 3.75 3.64 3.95-.23.2-.44.55-.51 1.07-.46.21-1.61.55-2.33-.66-.15-.24-.6-.83-1.23-.82-.67.01-.27.38.01.53.34.19.73.9.82 1.13.16.45.68 1.31 2.69.94 0 .67.01 1.3.01 1.49 0 .21-.15.45-.55.38A7.995 7.995 0 0 1 0 8c0-4.42 3.58-8 8-8Z"></path>
</svg>


