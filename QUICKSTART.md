# Быстрый старт

- Установить Docker
- `git clone https://github.com/suiljex/DestructiveFarm`
- `docker-compose up --build --detach`
- `docker-compose down`

## Обратить внимание

- Подготовить протокол для сдачи флагов в `server/protocols`
- Отредактировать `server/config.py`
- Прописать сервер фермы по умолчанию в `client/start_sploit.py` для удобства

## Может пригодиться

Обнуление базы данных фермы:

- `docker volume ls` для просмотра хранилищ
- `docker volume rm <name>` удалить хранилище

или просто `docker volume prune` удалить все хранилища