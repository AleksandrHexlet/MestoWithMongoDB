# MestoWithMongoDB
## Backend part for service for uploading photos
Версия 1.0.2 https://github.com/AleksandrHexlet/MestoWithMongoDB.git

RUS

Для развертывания проекта локально необходимо:
- скопировать репозиторий;
- выполнить команду npm install,
- запустить mongodb командой mongod,
- запустить сервер npm run start.
Сервер заупускается на http://localhost:3000/
Для выполнения запросов используйте Postman или другую подобную программу:
работа с пользователями
- GET /users возвращает всех пользователей из базы;
- GET /users/:userId возвращает конкретного пользователя;
- POST /users создаёт пользователя;
    в теле POST необходимо передавать JSON с полями name, about, avatar. (avatar - ссылка на картинку)
- PATCH /users/me — обновляет профиль;
    в теле PATCH необходимо передавать JSON с полями name, about.
- PATCH /users/me/avatar — обновляет аватар;
    в теле PATCH необходимо передавать JSON с полями avatar.
работа с карточками
- GET /cards возвращает все карточки всех пользователей;
- POST /cards создаёт карточку;
    в теле POST необходимо передавать JSON с полями name, link.(link - ссылка на картинку)
- DELETE /cards/:cardId — удалить карточку;
- PUT /cards/:cardId/likes — поставить лайк карточке;
- DELETE /cards/:cardId/likes — убрать лайк с карточки;
