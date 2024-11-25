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
Напишите простую программу на Python или Bash. Например, программа может выполнять простую симуляцию робота или даже выводить текущее время и дату или простое приветствие.



