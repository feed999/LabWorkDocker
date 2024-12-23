# Laba 3
Автор - Азимов Адам

## Лабораторная работа №3 - Работа с Docker

## Задача 1
- Сcылка на образ [https://hub.docker.com/feed999/custom-nginx/general .](https://hub.docker.com/repository/docker/feed999/custom-nginx/general)

## Задача 2
<p align="center"><img src="docs/example_1.png" /></p>

## Задача 3
<p align="center"><img src="docs/example_2.png" /></p>

### Объяснение проблемы:
- **Команда ss -tlpn**: покажет, что Nginx больше не слушает порт 8888 на хосте, так как конфигурация изменилась внутри контейнера.
- **Команда curl http://127.0.0.1:8888**: вернет ошибку, так как порт 8888 больше не соответствует перенаправленному порту в контейнере.

## Задача 4
<p align="center"><img src="docs/example_3.png" /></p>

## Задача 5
<p align="center"><img src="docs/example_4.png" /></p>

- Docker Compose по умолчанию ищет файл docker-compose.yaml, так как это имя файла по умолчанию.
- Поэтому будет запущен только сервис registry из файла docker-compose.yaml.
<p align="center"><img src="docs/example_5.png" /></p>
-скриншот от поля "AppArmorProfile" до "Driver".
<p align="center"><img src="docs/example_6.png" /></p>
-portainer c задеплоенным компоузом
<p align="center"><img src="docs/example_7.png" /></p>
- файл compose.yaml

```console
version: "3"
services:
  portainer:
    network_mode: host
    image: portainer/portainer-ce:latest
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock

  registry:
    image: registry:2
    ports:
      - "5000:5000"
```