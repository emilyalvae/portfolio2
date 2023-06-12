# Pasos para deploy render

## 1. Instalamos dependencias

```bash
pip install psycopg2-binary

pip install dj-database-url

pip install django-environ

pip install gunicorn
```

## 2. Configuramos variables 

```python
DEBUG=
SECRET_KEY=
DATABASE_URL=
```

```py
DATABASES = {'default' : dj_database_url.parse(env('DATABASE_URL'))}
```

## 3. Creamos nuestro requirements

```bash
pip freeze > requirements.txt
```

## 4. Creamos nuestra base de datos en render

Estamos usando postgres por defecto.

[render.com](https://render.com//)

## 5. Configuramos deploy en render.com

Guia:
https://www.youtube.com/watch?v=AgTr5mw4zdI&t=1885s