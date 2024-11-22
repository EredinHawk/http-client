# HTTP клиент
Эту работу можно посмотреть в моем портфолио - https://eredinhawk.ru/http-client

### Цель:
    Реализовать простой HTTP клиент для выполнения запроса к NASA Open API

### Задачи:
- [x] Сконструировать HTTP запрос с использованием пакетов net/http и net/url стандартной библиотеки Go;
- [x] Получить API KEY https://api.nasa.gov/;
- [x] Выполнить запрос к API https://github.com/nasa/apod-api;
- [x] Получить HTTP ответ и вывести из него только URL строку изображения.
<br><br/>

![alt text](/sheme.png)

### Установка
---
1. Клонируй репозиторий
```bash
https://github.com/EredinHawk/http-client.git
```
2. Перейди в созданную директорию
```bash
cd путь/до/директории
```
3. Получи API KEY
```bash
https://api.nasa.gov/
```
4. Создай .env файл в корне приложения
```bash
nano .env
```
5. В созданном файле .env вставь строку:
```bash
API_KEY=foo
где foo - ключ, который получен в пункте №3
```
6. Запусти исполняемый файл, который подходит для твоей системы:
```bash
    На примере mac OS
    ./run_macos
```

Сразу после запуска исполняемого файла сформируется URL, и инициализированный HTTP-клиент выполнит запрос к API. В случае успеха вернется HTTP-ответ с соответствующими заголовками и телом в формате JSON. 

Приложение декодирует (это действие на диаграмме пропущено) ответ во внутреннюю структуру языка и выведет на печать строку URL. (Вдаваться в подробности как устроен сервис NASA API не будем.)

Перейдя по адресу, получим ежедневно меняющуюся фотографию космоса.
