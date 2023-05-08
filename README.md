## Проект Kyttygram

Проект Kyttygram представляет из себя сервис, в котором вы можете зарегистрироваться и рассказать о своем любимом котике, добавить его фотографию, указать имя и год рождения, а также добавить его выдающиеся достижения
Backend часть написана на Django, Frontend на React

## Технологии
- Django rest_framework
- Django rest_framework_simplejwt
- React
- Pillow
- Git
- Docker
- NGINX
- GUNICORN
- SQLITE

## Как установить:

### Установка backend:

Клонировать репозиторий:
```
git clone git@github.com:rest2011/infra_sprint1.git
```

```
cd infra_sprint1
```

Создать и активировать виртуальное окружение:

```
python -m venv venv
```

```
source venv/bin/activate
```

```
python -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Создать супепользователя:

```
python manage.py createsuperuser 
```

### Установка frontend:
Установка Node.js:

```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - &&\
sudo apt-get install -y nodejs 
```


Перейдите в директорию infra_sprint1/frontend/, установите зависимости для фронтенд-приложения:

```
npm i 
```

## Как заполнить env:

Создайте файл .env в корневой директории проекта.
Откройте файл .env в текстовом редакторе и добавьте строку:

```
SECRET_KEY=<ваш секретный ключ> 
```
Сохраните файл .env.
В вашем коде Python вы можете получить значение переменной окружения SECRET_KEY, используя модуль os. Например, в файле settings.py:

```
import os

from dotenv import load_dotenv

load_dotenv()
SECRET_KEY = os.getenv('SECRET_KEY')
```

## Автор проекта

Хаматьяров Ринат
github.com/rest2011
