# docker_docker-compose

Для установки Docker и Docker Compose на Ubuntu, вам следует выполнить следующие шаги:

### Установка Docker на Ubuntu

1. **Установите необходимые пакеты для добавления репозитория Docker:**
   
    
    sudo apt update
    sudo apt install apt-transport-https ca-certificates curl software-properties-common
    

2. **Добавьте официальный GPG ключ Docker:**
   
    
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    

3. **Добавьте репозиторий Docker в список источников APT:**
   
    
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
    

4. **Установите Docker:**
   
    
    sudo apt update
    sudo apt install docker-ce
    

5. **Проверьте статус сервиса Docker:**
   
    
    sudo systemctl status docker
    

### Установка Docker Compose на Ubuntu

1. **Загрузите последнюю версию Docker Compose:**
   
    
    sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    

2. **Добавьте права на выполнение файла Docker Compose:**
   
    
    sudo chmod +x /usr/local/bin/docker-compose
    

3. **Проверьте установку Docker Compose:**
   
    
    docker-compose --version
    

Теперь у вас должны быть установлены Docker и Docker Compose на вашем сервере Ubuntu. Вы можете начать использовать их для развертывания контейнеров и управления приложениями.