My DevOps Project

This is my step into the world of DevOps.
My DevOps Project

Выполненные шаги

Часть 1: Установка Git и настройка GitHub
- Установлен Git на Ubuntu Server. Проверка: `git --version`.
- Сгенерирован и добавлен SSH-ключ в аккаунт GitHub для безопасного подключения.

Часть 2: Работа с GitHub
- Создан публичный репозиторий `my-first-devops`.
- Репозиторий клонирован на локальную машину через SSH.

Часть 3: Установка и работа с Docker
- Docker успешно установлен по официальной инструкции.
- Проверка: `docker --version`.
- Запущен тестовый контейнер `hello-world` для проверки корректности установки.

Часть 4: Создание собственного Docker-образа
- Создан `Dockerfile` для запуска простого Python-скрипта.
- Создан файл `script.py`, который выводит сообщение "Hello, DevOps World!".
- Образ успешно собран с тегом `my-python-app`.
- Контейнер запущен и вывел ожидаемое сообщение.

  
Скриншоты: 
 <p align="center">
  <img src="scrshts/Hello_from_docker.png" alt="Hello from Docker" width="600"/>
  <br>
  <em>Hello from Docker - запуск команды docker run hello-world</em>
</p>

<p align="center">
  <img src="scrshts/Hello%2C%20DevOps%20World%21.png" alt="Hello DevOps World" width="600"/>
  <br>
  <em>Hello, DevOps World! - контейнер со скриптом python</em>
</p>
