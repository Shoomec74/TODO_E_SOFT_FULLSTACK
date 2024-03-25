# ["BotKits дипломный проект Coral 14 Web+"](https://botkits.nomoreparties.co)

## IP адрес __84.201.178.186__
## Frontend https://botkits.nomoreparties.co
## Swagger https://botkits.nomoreparties.co/api/docs
***
### Работа с подмодулями

Добавление подмодуля
```
git submodule add [URL репозитория] [путь/до/директории]
```
Зафиксируйте изменения в подмодуле
```
cd [путь/до/подмодуля]
git add .
git commit -m "Made changes in submodule"
git push
```
Обновите ссылку на подмодуль в главном репозитории
```
cd ..  # Вернитесь в корневую директорию главного репозитория
git add [путь/до/подмодуля] #для обновления ссылки на подмодуль
git commit -m "Updated submodule"
git push
```
Клонирование репозитория с подмодулями 
```
git clone [URL репозитория] --recursive
```
Обновить подмодули следующим образом
```
git pull
git submodule update --init --recursive
```

