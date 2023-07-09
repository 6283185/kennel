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
![diagramm](https://github.com/6283185/kennel/blob/main/Task%206.png?raw=true)

7. В подключенном MySQL репозитории создать базу данных Друзья
человека

	sudo mysql -u root -p

	CREATE DATABASE friends_of_human;
	
8. Создать таблицы с иерархией из диаграммы в БД

CREATE TABLE cat (
	id INT PRIMARY KEY AUTO_INCREMENT,
	animal_name CHAR(30),
    commands TEXT,
    date_of_birth DATE
);

CREATE TABLE dog (
	id INT PRIMARY KEY AUTO_INCREMENT,
	animal_name CHAR(30),
    commands TEXT,
    date_of_birth DATE
);

CREATE TABLE hamster (
	id INT PRIMARY KEY AUTO_INCREMENT,
	animal_name CHAR(30),
    commands TEXT,
    date_of_birth DATE
);

CREATE TABLE horse (
	id INT PRIMARY KEY AUTO_INCREMENT,
	animal_name CHAR(30),
    commands TEXT,
    date_of_birth DATE
);

CREATE TABLE camel (
	id INT PRIMARY KEY AUTO_INCREMENT,
	animal_name CHAR(30),
    commands TEXT,
    date_of_birth DATE
);

CREATE TABLE donkey (
	id INT PRIMARY KEY AUTO_INCREMENT,
	animal_name CHAR(30),
    commands TEXT,
    date_of_birth DATE
);
	
9. Заполнить низкоуровневые таблицы именами(животных), командами
которые они выполняют и датами рождения

INSERT INTO cat (animal_name,commands, date_of_birth) VALUES 
	('barsik', 'meow', '2021-01-01'),
	('kosh', 'meow, stand', '2019-12-10'),
    ('frank', 'meow, wlow', '2020-02-02'),
    ('dir', 'meow', '2022-03-03'),
    ('krop', 'meow', '2018-05-05');
   
INSERT INTO dog (animal_name,commands, date_of_birth) VALUES 
	('wolf', 'flufy', '2021-01-01'),
	('ralf', 'site', '2019-12-10'),
    ('qwerty', 'left hand', '2020-02-02'),
    ('asdfg', 'right hand', '2022-03-03'),
    ('red', 'meow', '2018-05-05');
    
INSERT INTO hamster (animal_name,commands, date_of_birth) VALUES 
	('crack', 'eat', '2021-01-01'),
	('jisus', 'eat', '2019-12-10'),
    ('qwerty', 'left hand', '2020-02-02'),
    ('asdfg', 'right hand', '2022-03-03'),
    ('black', 'meow', '2018-05-05');
    
INSERT INTO horse (animal_name,commands, date_of_birth) VALUES 
	('igogo', 'eat', '2021-01-01'),
	('igaga', 'eat', '2019-12-10'),
    ('ijoho', 'left hand', '2020-02-02'),
    ('jijij', 'right hand', '2022-03-03'),
    ('aoaoaa', 'meow', '2018-05-05');
    
INSERT INTO camel (animal_name,commands, date_of_birth) VALUES 
	('qwea', 'eat', '2021-01-01'),
	('dsaf', 'eat', '2019-12-10'),
    ('gfdsdf', 'left hand', '2020-02-02'),
    ('grwtw', 'right hand', '2022-03-03'),
    ('werqr', 'meow', '2018-05-05');
    
INSERT INTO donkey (animal_name,commands, date_of_birth) VALUES 
	('stup', 'eat', '2021-01-01'),
	('tupi', 'eat', '2019-12-10'),
    ('upid', 'left hand', '2020-02-02'),
    ('task', 'right hand', '2022-03-03'),
    ('done', 'meow', '2018-05-05');

10. Удалить из таблицы верблюдов, т.к. верблюдов решили перевезти в другой
питомник на зимовку. Объединить таблицы лошади, и ослы в одну таблицу.

TRUNCATE camel;
INSERT INTO horse (animal_name, commands, date_of_birth)
SELECT animal_name, commands, date_of_birth
FROM donkey;

DROP TABLE donkey;

RENAME TABLE horse TO horse_donkey;

11.Создать новую таблицу молодые животные в которую попадут все
животные старше 1 года, но младше 3 лет и в отдельном столбце с точностью
до месяца подсчитать возраст животных в новой таблице

CREATE TABLE young_animal (
	id INT PRIMARY KEY AUTO_INCREMENT,
	animal_name CHAR(30),
    commands TEXT,
    date_of_birth DATE,
    age TEXT
);


DELIMITER $$
CREATE FUNCTION age_animal (date_b DATE)
RETURNS TEXT
DETERMINISTIC
BEGIN
    DECLARE res TEXT DEFAULT '';
	SET res = CONCAT(
            TIMESTAMPDIFF(YEAR, date_b, CURDATE()),
            ' years ',
            TIMESTAMPDIFF(MONTH, date_b, CURDATE()) % 12,
            ' month'
        );
	RETURN res;
END $$
DELIMITER ;

INSERT INTO young_animal (animal_name, commands, date_of_birth, age)
SELECT animal_name, commands, date_of_birth, age_animal(date_of_birth)
FROM cat
WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) BETWEEN 1 AND 3
UNION ALL
SELECT animal_name, commands, date_of_birth, age_animal(date_of_birth)
FROM dog
WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) BETWEEN 1 AND 3
UNION ALL
SELECT animal_name, commands, date_of_birth, age_animal(date_of_birth)
FROM hamster
WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) BETWEEN 1 AND 3
UNION ALL
SELECT animal_name, commands, date_of_birth, age_animal(date_of_birth)
FROM horse_donkey
WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) BETWEEN 1 AND 3;

SET SQL_SAFE_UPDATES = 0;

DELETE FROM cat 
WHERE TIMESTAMPDIFF(YEAR, cat.date_of_birth, CURDATE()) IN (1, 2, 3);

DELETE FROM dog 
WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) BETWEEN 1 AND 3;

DELETE FROM hamster 
WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) BETWEEN 1 AND 3;

DELETE FROM horse_donkey 
WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) BETWEEN 1 AND 3;

CREATE TABLE animals (
	id INT PRIMARY KEY AUTO_INCREMENT,
	animal_name CHAR(30),
    commands TEXT,
    date_of_birth DATE,
    age TEXT,
    animal_type ENUM('cat','dog','hamster', 'horse_donkey', 'young_animals') NOT NULL
);

INSERT INTO animals (animal_name, commands, date_of_birth, age, animal_type)
SELECT animal_name, commands, date_of_birth, age_animal(date_of_birth), 'cat'
FROM cat;

INSERT INTO animals (animal_name, commands, date_of_birth, age, animal_type)
SELECT animal_name, commands, date_of_birth, age_animal(date_of_birth), 'dog'
FROM dog;

INSERT INTO animals (animal_name, commands, date_of_birth, age, animal_type)
SELECT animal_name, commands, date_of_birth, age_animal(date_of_birth), 'hamster'
FROM hamster;

INSERT INTO animals (animal_name, commands, date_of_birth, age, animal_type)
SELECT animal_name, commands, date_of_birth, age_animal(date_of_birth), 'horse_donkey'
FROM horse_donkey;

INSERT INTO animals (animal_name, commands, date_of_birth, age, animal_type)
SELECT animal_name, commands, date_of_birth, age_animal(date_of_birth), 'young_animals'
FROM young_animal;
