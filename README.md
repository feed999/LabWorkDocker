# Laba 3
Автор - Азимов Адам

## Лабораторная работа №3 - Работа с Docker

## Задача 1
- Сcылка на образ [https://hub.docker.com/USERNAME/custom-nginx/general .](https://hub.docker.com/repository/docker/feed999/custom-nginx/general)

## Задача 2
<p align="center"><img src="docs/example_1.png" /></p>

## Задача 3
<p align="center"><img src="docs/example_2.png" /></p>

### Объяснение проблемы:
- **Команда ss -tlpn**: покажет, что Nginx больше не слушает порт 8080 на хосте, так как конфигурация изменилась внутри контейнера.
- **Команда curl http://127.0.0.1:8888**: вернет ошибку, так как порт 8080 больше не соответствует перенаправленному порту в контейнере.