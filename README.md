# api_final
api final

# Описание
Данный проект позволяет с помощью API создавать посты, писать к ним комментарии, а также
подписываться на других пользователей.

# Установка
1. Клонировать репозиторий и перейти в него в командной строке
    ```bash
    git clone <ссылка на репозиторий>

    cd api_final_yatube/
    ```

2. Cоздать и активировать виртуальное окружение:
    ```bash
    python3 -m venv env

    source env/bin/activate
    ```

Если у вас Windows, то процесс будет таким:
    ```bash
    python -m venv env
    source env/Scripts/activate
    ```

3. Обновить pip. Далее установить зависимости из файла requirements.txt:
    ```bash
    python3 -m pip install --upgrade pip

    pip install -r requirements.txt
    ```

Если у вас Windows, то процесс будет таким:
    ```bash
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

4. Выполнить миграции:
    ```bash
    python3 manage.py migrate
    ```

Если у вас Windows, то процесс будет таким:
    ```bash
    python manage.py migrate
    ```

5. Перейти в папку с проектом и запустить проект:
    ```bash
    cd yatube_api/

    python3 manage.py runserver
    ```

Если у вас Windows, то процесс будет таким:
    ```bash
    cd yatube_api/
    python manage.py runserver
    ```

# Примеры запросов API
## Получение публикаций
При GET запросе:
    ```bash
    http://127.0.0.1:8000/api/v1/posts/
    ```

В случае успешного запроса, вернется примерный ответ:
    ```bash
    [
        {
            "id": 1,
            "author": "string",
            "text": "string",
            "pub_date": "2025-05-14T16:25:12.404929Z",
            "image": null,
            "group": null
        },
    ]
    ```
## Создание публикации
При POST запросе:
    ```bash
    http://127.0.0.1:8000/api/v1/posts/
    ```

С примерными данными:
    ```bash
    {
        "text": "string",
        "image": "string",
        "group": 0
    }
    ```

В случае успешного добавления вернется примерно такой ответ:
    ```bash
    {
        "id": 1,
        "author": "string",
        "text": "string",
        "pub_date": "2019-08-24T14:15:22Z",
        "image": "string",
        "group": 1
    }
    ```

# Документация
Для более подробной информации о запросах перейдите в документацию
    ```bash
    http://127.0.0.1:8000/redoc/
    ```
