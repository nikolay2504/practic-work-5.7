# practic-work-5.7
<h1> Шаги выполнения практической работы. <hr>

<h1> 1. Установка Docker и Docker Compose:
    
1.1 Установите Docker и Docker Compose на вашу систему.


  Процесс:
 <h2> a. Обновил индекс пакетов:
  sudo apt-get update
<h2> b. Установите необходимые пакеты:
sudo apt-get install ca-certificates curl gnupg
<h2> c. Добавьте официальный GPG-ключ в Docker:
sudo install -m 0755 -d /etc/apt/keyrings curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg sudo chmod a+r /etc/apt/keyrings/docker.gpg
<h2> d. Добавил репозиторий Docker в источники Apt:
echo \
"deb [arch="$(dpkg --print-architecture)"
signed-by=/etc/apt/keyrings/docker.gpg]
https://download.docker.com/linux/ubuntu \
"$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
<h2> e. Обновил индекс пакетов:
sudo apt-get update
<h2> f. Установка пакетов Docker
    
Чтобы установить последнюю версию, выполнил:
sudo apt-get install docker-ce docker-ce-cli containerd.io
docker-buildx-plugin docker-compose-plugin
<h2> g. Проверка установки
    
    С помощью команды docker run hello world запустил контейнер, который создан из образа hello world. sudo docker run hello-world
    
<h1> 1.2 Настройте Docker для работы без прав root (добавление пользователя в группу docker).
  
<h2> a. Создал группу docker: sudo groupadd docker
<h2> b. Добавил пользователя в группу docker: sudo usermod -aG docker $USER
<h2> c. Вышел из системы и вошёл снова, чтобы изменения вступили в силу.
<h2> d. Проверил, что команды docker теперь работают без sudo: docker run hello-world
<h2> e. Проверка версии Docker Compose: docker-compose --version

<h1> 2. Разработка простой программы:
<h1> 2.1. Напишите простую программу на Python или Bash. Например, программа может выполнять простую симуляцию робота или даже выводить текущее время и дату или простое приветствие.
    
<h1> 2.2 Создайте репозиторий на GitHub для вашего проекта.
Ссылка на репозиторий GitHub: https://github.com/nikolay2504/practic-work-5.7

<h1> 3. Создание Docker-образа для программы:
<h1> 3.1 Создал Dockerfile для сборки образа, включающего программу и зависимости.
<h1> 3.2 Соберите Docker-образ из вашего Dockerfile.

    nikolay@niko-RV411:~/pr5$ docker build -t pr5 .
<h1> 4. Запуск и тестирование Python-приложения в Docker-контейнере:
<h1> 4.1 Запустите Docker-контейнер из созданного образа.
    
Запустил docker run -it pr5 /bin/bash
<h1> 4.2 Проверьте, что ваша программа работает корректно внутри контейнера.
    
Запустил программу praktika5.bash из папки home/ (программа выводит текущую дату и время):

<h1> 5. Работа с Docker Compose:
<h1> 5.1 Создайте docker-compose.yml, который запускает ваш Docker-контейнер с программой.

    создал файл docker-compose.yaml в папке pr5. 
<h1> 5.2 Добавьте комментарии в docker-compose.yml, объясняющие его структуру и команды.
<h1> 5.3 Убедитесь, что Docker Compose позволяет запустить ваш контейнер.

    Выполнено. Запускается, см. скриншоты.
    
  
 <h1> 6. Оформление проекта на GitHub:
<h1> 6.1 Поместите ваш Dockerfile и docker-compose.yml в репозиторий на GitHub.
<h1> 6.2 Подготовьте README.md, описывающий ваш проект и процесс запуска программы с помощью Docker и Docker Compose.

