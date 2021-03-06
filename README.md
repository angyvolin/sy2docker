Symfony Docker Edition
========================

Ідея проекту - запустити [Symfony][1], при цьому не захламити ніякими пакетами власний комп'ютер. Все, що необхідно - це git, docker та docker-compose.

Встановлення та запуск
--------------

Встановлюємо [Docker][2] та [Docker Compose][3]

Клонуємо репозиторій

```bash
$ git clone git@github.com:madman/sy2docker.git
```

або 

```bash
composer create-project --no-install --no-scripts madman/sy2docker
```
  
Виставляємо необхідні права на папки та файли

```bash
$ bin/init
```

Збираємо образи для docker

```bash
$ docker-compose build
```

Запускаємо контейнери

```bash
$ docker-compose up -d
```

Встановлюємо залежності

```bash
$ docker-compose run composer install 
```

Відкриваємо в браузері [http://localhost:8080/](http://localhost:8080/)


Які є контейнери?
--------------

  * nginx - 1.10.1
  * fpm - php-fpm (версія php 5.6.30)
  * mysql - версия 5.5
  * composer - сервіс для роботи з композером
  * console - консоль symfony

Відмінність від [Symfony Standard Edition][4]
--------------

  * видалений пакет SwiftmailerBundle

  * видалений пакет incenteev/composer-parameter-handler. Налаштування відбувається автоматично

Все програмне забезпечення в Symfony Docker Edition розповсюджується під MIT або BSD ліцензіями

Насолоджуйтесь!

[1]:  https://symfony.com/doc/3.2/setup.html
[2]:  https://docs.docker.com/engine/installation/
[3]:  https://docs.docker.com/compose/install/
[4]:  https://github.com/symfony/symfony-standard