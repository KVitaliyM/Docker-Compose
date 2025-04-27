### Задача:
Создать два стека:
1. Flask+redis – веб-приложение со счетчиком входов
2. Prometheus+grafana – сервер мониторинга

### Ход выполнения:
1. Устанавливаем compose

```
sudo apt update
sudo apt install docker-compose-v2
```

2. Создаем каталог для проекта

![compose1](https://github.com/user-attachments/assets/2d64e2a5-380b-4a31-b2b6-1887eabd577d)

3. Создаем веб-приложение (app.py)

![compose2](https://github.com/user-attachments/assets/966d51de-0155-42cb-9032-00c0e9ed660b)

4. Объявляем зависимости для python

![compose3](https://github.com/user-attachments/assets/6eaf3d14-faec-478e-93b8-3e83a2ac977d)

5. Создаем dockerfile для контейнера с flask

![compose4](https://github.com/user-attachments/assets/7a6243b9-5ff2-424f-9dbc-aa87126bc3d3)

6. Создаем compose.yaml – описание 2х сервис-контейнеров

![compose5](https://github.com/user-attachments/assets/33d08edb-6e1b-4bb2-a1c4-2415e0b8585f)

7. Запускаем оба сервис-контейнера Flask+Redis

![compose6](https://github.com/user-attachments/assets/02a374fa-e408-46c4-84d2-24354f3f843b)

8. Проверка стека Flask+redis

![compose7](https://github.com/user-attachments/assets/ff5259de-f054-40cf-bc8f-be2891559091)
![compose8](https://github.com/user-attachments/assets/c04091c3-70b1-426c-ba11-e8e5cd1996c1)
![compose8_1](https://github.com/user-attachments/assets/27f768e2-7803-4456-b071-a176088f5361)

9. Собираем мониторинг (prometheus+grafana)

![compose9](https://github.com/user-attachments/assets/3808949f-c9a0-42d8-ac73-5ca37b12820e)

10. Создаем compose.yaml для Prometheus+Grafana

![compose10](https://github.com/user-attachments/assets/89d9d7e8-5546-43ca-9b41-e1eac7921269)

11. Создаем конфиг для prometheus

![compose11](https://github.com/user-attachments/assets/1a9521f2-fff6-48bc-b3f9-4990cf2c53e6)

12. Создаем конфиг для grafana

![compose12](https://github.com/user-attachments/assets/a2b2dab8-7663-4156-b4d1-e96bc915da35)

13. Запускаем оба сервис-контейнера Prometheus+Grafana

![compose13](https://github.com/user-attachments/assets/7ebd67cd-e1a9-424d-9a56-665ff420a5b3)

14. Проверка мониторинга Prometheus+Grafana

![compose13_1](https://github.com/user-attachments/assets/2d629155-77ba-47a3-94b0-e2b5430bcab4)
![compose14](https://github.com/user-attachments/assets/fe961475-8bde-4426-906f-587b1410c285)

15. Смотрим метрику самого Prometheus

![compose15](https://github.com/user-attachments/assets/52e9425b-3fc0-4505-bd30-7774714c041a)

16. Добавляем мониторинг нашего Flask-приложения (и не только)

![compose16](https://github.com/user-attachments/assets/15c6fffd-3864-482e-8ed4-ae0ce7d39a77)
![compose17_замена](https://github.com/user-attachments/assets/7609cd53-1f7d-43d9-9151-1b41af3c142a)

17. Пересобираем стек мониторинга

![compose18](https://github.com/user-attachments/assets/fa6d0661-2547-4e03-83c7-4ea30c5f71da)
![compose19](https://github.com/user-attachments/assets/1f3cb93b-5c82-4c59-b2c4-bca67d76453f)

18. Проверка экспортера

![compose20](https://github.com/user-attachments/assets/1f931905-815c-4efd-a273-347739e7f5fe)
![compose21](https://github.com/user-attachments/assets/50c697f9-f2f6-4edd-9a77-b77209f5ce70)

19. Создаем дашборд

![compose22](https://github.com/user-attachments/assets/f65661f9-a958-4e79-b782-c979ee543beb)
![compose23](https://github.com/user-attachments/assets/320e772e-3535-4904-ada8-d2f245243f9f)
![compose24](https://github.com/user-attachments/assets/0af17415-cccf-4d18-bb12-9ae94e4bdfa6)
