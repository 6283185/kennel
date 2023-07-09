Задание 1. Используя команду cat в терминале операционной системы Linux, создать два фаила 
Домашние животные (заполнив файл собаками, кошками, хомяками)
 и Вьючные животными заполнив файл Лошадьми, верблюдами и ослы), а затем объединить их.
 Просмотреть содержимое созданного фаила. Переименовать фаил, дав ему новое имя (Друзья человека). 

    cat > pets.txt
    cat > work_animals.txt
    cat pets.txt work_animals.txt > animals.txt

2. Создать директорию, переместить файл туда. 

    mkdir animals
    mv friends_of_human.txt animals/
	
3. Подключить дополнительный репозиторий MySQL. Установить любой пакет
из этого репозитория.

	wget https://dev.mysql.com/get/mysql-apt-config_0.8.24-1_all.deb
	sudo dpkg -i mysql-apt-config_0.8.24-1_all.deb
	
4. Установить и удалить deb-пакет с помощью dpkg.

	wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-j_8.0.32-1ubuntu22.04_all.deb
	sudo dpkg -i mysql-connector-j_8.0.32-1ubuntu22.04_all.deb
	
	Удалить: 
	sudo dpkg -r mysql-connector-j
5. Выложить историю команд в терминале ubuntu

	mkdir kennel
    cd kennel
    cat > pets.txt
    git add .
    git status
    git commit -am "initial"
    git push
    git remote add origin https://github.com/6283185/kennel.git
    git branch -M main
    git push -u origin main
    cat > work_animals.txt
    git commit -am "work animals"
    git add .
    git commit -am "work animals"
    git push
    cat pets.txt work_animals.txt > animals.txt
    ls -l
    cat animals.txt
    git add .
    git push
    git commit -am "pets & work animals to animals"
    mv all_animals.txt friends_of_human.txt
    mv animals.txt friends_of_human.txt
    git add .
    git commit -am "rename animals to friens of human"
    mkdir animals
    mv friends_of_human.txt animals/
    git add .
    git commit -am "mkdir animals & put in animals.txt"
    sudo dpkg -i mysql-apt-config_0.8.24-1_all.deb
    git status
    git add .
    git push
    wget https://dev.mysql.com/get/mysql-apt-config_0.8.24-1_all.deb
    sudo dpkg -i mysql-apt-config_0.8.24-1_all.deb
    sudo apt-get update
    sudo apt-get install mysql-server
    systemctl status mysql
    wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-j_8.0.32-1ubuntu22.04_all.deb
    sudo dpkg -i mysql-connector-j_8.0.32-1ubuntu22.04_all.deb    
    sudo dpkg -r mysql-connector-j
    sudo apt-get autoremove
    
6. Нарисовать диаграмму, в которой есть класс родительский класс, домашние
животные и вьючные животные, в составы которых в случае домашних
животных войдут классы: собаки, кошки, хомяки, а в класс вьючные животные
войдут: Лошади, верблюды и ослы).
