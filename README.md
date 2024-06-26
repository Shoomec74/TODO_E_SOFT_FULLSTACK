# ["TODO E-SOFT TASK"](https://cleanwaveapp.ru)

## [Frontend code](https://github.com/Shoomec74/e_soft_front)
## [Backend code](https://github.com/Shoomec74/e_soft_task)
## [Скринкаст проекта](https://youtu.be/Akc-zKVavVc)

***

# Веб-приложение списка задач (TODO list).

Ссылка на репозиторий фронтенд части проекта **[GitHub](https://github.com/Shoomec74/e_soft_front)**

## Обзор

Проект представляет собой веб-приложение, предназначенное для помощи пользователям в планировании их активностей и управлении работой их подчинённых через систему управления задачами. Это позволяет создавать, обновлять и отслеживать задачи, обеспечивая эффективный способ организации рабочих нагрузок и сроков. Выполнено в рамках тестового задания от компании E-Soft.

## Особенности

- **Панель администратора:** Функционал суперадминистратора. Управление пользователями включая распределения подчиненных к руководителям. В будущем будет реализовано обновление и пользователей и миграции подчиненных от одного руководителя к другому.
- **Управление задачами:** Пользователи могут создавать, обновлять и отслеживать задачи с такими атрибутами, как заголовок, описание, сроки выполнения, приоритеты и статусы.
- **Управление пользователями:** Пользователи могут регистрироваться с их деталями, включая имя, фамилию, отчество, логин и пароль. Каждому пользователю можно назначить задачи и иметь подчинённых.
- **Страница авторизации:** Безопасный механизм входа для обеспечения защиты доступа к задачам и функциям управления.
- **Страница задач:** Задачи могут быть показаны с различными фильтрами, включая по дате завершения, ответственному лицу или без группировки, отсортированные по последнему обновлению.

Проект настроен с использованием следующих технологий:

- __React TS__ для фронтенда
- __Redux Toolkit__ для управления состоянием
- __Material UI__ для стилизации компонентов
- __Moment.js__ для манипуляций с датами
- __CASL__ для управления правами доступа

***

# Бэкенд чать проекта для Веб-приложения списка задач (TODO list).

Ссылка на Бэкенд часть приожение на __[GitHub](https://github.com/Shoomec74/e_soft_task)__

## Обзор

Проект представляет собой API и хранение информаци о пользователях и их задачах в базе данных Postgres, предназначенное для помощи пользователям в планировании их активностей и управлении работой их подчинённых через систему управления задачами. Это позволяет создавать, обновлять и отслеживать задачи, обеспечивая эффективный способ организации рабочих нагрузок и сроков. Выполнено в рамках тестового задания от компании E-Soft.

Проект настроен с использованием следующих технологий:

- __NEST__ для API
- __JWT__ авторизация с контрлем чернотго списка токенов и обновления токена по Redresh токену
- __TYPE ORM__ для управления базой данных в данном проекте Postgres
- __CASL__ для управления правами доступа

***

## Запуск проекта TODO E-SOFT TASK в Docker локально

**Шаг 1. Склогнируйте репозиторий.**
```
git clone https://github.com/Shoomec74/TODO_E_SOFT_FULLSTACK.git --recursive
```

**Шаг 2. Обновить подмодули следующим образом**
```
git pull
```
следом
```
git submodule update --init --recursive
```

**Шаг 3. Создайте .env файл в корне папки frontend**
```
REACT_APP_URL_PROD=http://localhost:4000 #Отправляем запросы на контейнер с бэкендом
```
**Шаг 4. Создайте .env файл в корне проекта TODO_E_SOFT_FULLSTACK**
```yaml
# === Для работы приложения ===
APP_PORT=                                  # Порт, на котором будет слушать ваше приложение. Например 3000
GLOBAL_PREFIX=                             # Глобальный префикс для всех маршрутов приложения. В данном случае api
LOGIN_SUPERADMIN=api                       # Логин суперадмина приложения. Любая строка которую вы будете вводитьв поле логина при входе в приложение
PASSWORD_SUPERADMIN=                       # Пароль суперадмина. Любая строка которую вы будете вводить в поле с паролем при входе в приложение
JWT_EXPIRES=                               # Время жизни JWT. Например 30m. Поддерживает от секунды до дня 1s, 1m, 1h, 1d
REFRESHTOKEN_EXPIRESIN=                    # Время жизни токена обновления. Например 1h. Поддерживает от секунды до дня 1s, 1m, 1h, 1d
JWT_SECRET=                                # Секретный ключ для JWT (JSON Web Tokens). Секретная строка для дешифровки токена
ALLOW_URL=http://localhost:8081            # Одобренный урл с которого доапускается обращения к серверу. В данном случае http://localhost:8081

# === Для базы данных ===
DB_TYPE=                                   # Тип базы данных. Например postgres
DB_HOST=db                                 # Хост базы данных. Например localhost для локального подключения к БД или имя контейнера например db если БД в Docker
DB_PORT=                                   # Порт для подключения к базе данных. Например 5432
DB_USERNAME=                               # Имя пользователя для подключения к базе данных. Например root
DB_PASSWORD=                               # Пароль для подключения к базе данных. Например root
DB_NAME=                                   # Имя базы данных. Например dbSupername

# === Для docker compose ===
BACK_PORT_CONTAINER=4000                   # Порт контейнера с бекендом. Не забудьте если вы заменили порт то замените его в env файле в папке frontend
FRONT_PORT_CONTAINER=8080                  # Порт контейнера с фронтендом. Если замените то не забудьте поменять порт в ALLOW_URL
BACK_APP_PORT=3000                         # Порт который слушает бэкенд приложение
FRONT_APP_PORT=80                          # Порт который будет слушать nginx контейнера и отдавать фронтенд
```
**Шаг 5. Запустите сбоку контецйнеров**
```
docker compose up -d
```
После успешного разворачивания приложения перейдите на http://localhost:8080 и начните работать с приложением
