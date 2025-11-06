My DevOps Project

This is my step into the world of DevOps.
My DevOps Project

Выполненные шаги
Часть 0: Настройка виртуальной машины
Создана виртуальная машина с Ubuntu Server 22.04 LTS в VirtualBox
Настроено подключение по SSH через PuTTY


Часть 1: Установка Git и настройка GitHub
Установлен Git на Ubuntu Server
Сгенерирован SSH-ключ RSA для безопасного подключения к GitHub
Настроена аутентификация с GitHub


Часть 2: Работа с GitHub
Создан публичный репозиторий -my-first-devops.
Создан файл README.md с базовым описанием
Репозиторий клонирован на сервер через SSH


Часть 3: Установка и работа с Docker
Docker успешно установлен по официальной инструкции
Добавлен официальный GPG-ключ Docker
Настроен репозиторий Docker
Запущен тестовый контейнер hello-world


Часть 4: Создание собственного Docker-образа
Создан Dockerfile для запуска Python-скрипта
Создан файл script.py с выводом сообщения
Собран Docker-образ с тегом my-python-app
Контейнер успешно запущен и вывел ожидаемое сообщение


Проблемы и их решение


1. Проблема: После установки виртуальная машина не имела доступа к интернету, что препятствовало установке необходимых пакетов.
Решение:
Изменен тип сетевого подключения в VirtualBox с NAT на Сетевой мост (Bridged Adapter)
После изменения настроек сеть заработала корректно

2. Проблема с генерацией и копированием SSH-ключа
Проблема:
При первой попытке выполнения cat ~/.ssh/id_ed25519.pub возникала ошибка no such file or directory
Отсутствовал доступ к мыши в виртуальной машине, что затрудняло копирование ключа
Решение:
Сгенерирован новый SSH-ключ с использованием алгоритма RSA: ssh-keygen -t rsa -b 4096
Для копирования ключа использован Python HTTP-сервер:
                  BASH
cat ~/.ssh/id_rsa.pub > /tmp/my_ssh_key.pub
cd /tmp
python3 -m http.server 8000
Ключ скачан через браузер с основного компьютера


3. Проблема с клонированием репозитория (Невнимательность)
Проблема: При первой попытке подключения к GitHub возникало предупреждение о неизвестном хосте.
Решение:
Подтверждено подключение введением yes при запросе:
The authenticity of host 'github.com' can't be established...
Are you sure you want to continue connecting (yes/no/[fingerprint])?

4. Проблема с отсутствием Dockerfile
Проблема: При первой попытке сборки Docker-образа возникала ошибка:
Текст из терминала:
ERROR: failed to build: failed to solve: failed to read dockerfile: open Dockerfile: no such file or directory
Решение:
Вручную созданы файлы Dockerfile и script.py в папке репозитория
Использован текстовый редактор nano для создания файлов


   Заключение
  
Все этапы проекта успешно завершены. В процессе выполнения были решены различные проблемы конфигурации, 
что позволило получить практический опыт в настройке DevOps-окружения.
Проект демонстрирует полный цикл: от настройки инфраструктуры до развертывания приложения в контейнере.**

  
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
