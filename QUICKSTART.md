# Быстрый старт

- Установить Docker
- `git clone https://github.com/suiljex/DestructiveFarm`
- `docker-compose up --build --detach`
- `docker-compose down`

## Обратить внимание

- Подготовить протокол для сдачи флагов в `server/protocols`
- Отредактировать `server/config.py`

  ``` python
    'TEAMS': {'Team #{}'.format(i): '10.0.0.{}'.format(i)
              for i in range(1, 29 + 1)},
    'FLAG_FORMAT': r'[A-Z0-9]{31}=',

    'SYSTEM_PROTOCOL': 'ructf_tcp',
    'SYSTEM_HOST': '127.0.0.1',
    'SYSTEM_PORT': 31337,
    ...
  ```

- Прописать сервер фермы по умолчанию в `client/start_sploit.py` для удобства

  ``` python
    parser.add_argument('-u', '--server-url', metavar='URL',
                    default='http://farm.kolambda.com:5000',
                    help='Server URL')
  ```

## Может пригодиться

- Все данные хранятся в `./.data`
