# Инструкции для запуска приложения

## Запуск клиентской части

1. Считая, что вы находитесь в корне проекта, перейти в папку с клиентской частью приложения:

   - `cd client`

2. Запустить ReactApp в dev режиме (При первом запуске не забудьте предварительно загрузить все пакеты: `npm i`):

   - `npm start`

- Приложение будет доступно в браузере по адресу [http://localhost:3000](http://localhost:3000) (или на другом свободном порту).

## Запуск серверной части (в т.ч. серверов баз данных)

1. (Один раз). <br>
   Вам понадобится новый терминал. <br>
   Установить приложение для контейнеризации [Docker](https://docs.docker.com/):

   - [Ubuntu](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository) (выполнить 3 шага)
   - [Windows](https://docs.docker.com/docker-for-windows/install/)
   - [Mac](https://docs.docker.com/docker-for-mac/install/)

   и [Docker Compose](https://docs.docker.com/compose/install/) (выбрать нужную ОС).

1. (Каждый раз). <br>
   Вам понадобится еще один новый терминал. <br>
   Для запуска серверной части приложения (+ серверов баз данных) в корневой папке проекта запустить скрипт:

   - `./start-back-dev.sh`

   (Для Windows: в корне проекта выполнить в терминале `docker-compose --file docker-compose-only-back-dev.yaml up`)

## Примечания

- При работе приложения в dev-режиме понадобятся данные тестовых банковских карт:

  - для оплаты работы с карты buyer`а при создании контеста:
    - Card number: 4111111111111111
    - Expires end: 09/23
    - cvc/cvv: 505
  - для вывода средств на карту creator`а:
    - Card number: 5105105105105100
    - Expires end: 09/23
    - cvc/cvv: 510
