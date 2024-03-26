# ["TODO E-SOFT TASK"](https://botkits.nomoreparties.co)

## [Frontend code](https://github.com/Shoomec74/e_soft_front)
## [Backend code](https://github.com/Shoomec74/e_soft_task)
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

## Запуск в режиме разработки

**Локально в Docker** - соберет приложение в контейнерах.

```
docker compose up -d
```



