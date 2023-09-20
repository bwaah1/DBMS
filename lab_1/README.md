# Лабораторна 1
#### Інсталяція СУБД SQL та noSQL 

## Інсталяція mySQL на Linux Ubuntu
**Крок 1:** Переходимо до терміналу та за допомогою команди встановлюємо MySQL :
```sh
sudo apt install mysql-server
```
Вводимо пароль і натискаємо ENTER.

**Крок 2:** Натискаємо "y", щоб продовжити.

**Крок 3:** Щоб перевірити встановлення або дізнатися версію, вводимо команду :
```sh
mysql --version
```
**Step 4:** Тепер ми налаштуємо компонент VALIDATE PASSWORD :

```sh 
sudo mysql_secure_installation
```


Потім натискаємо "y", щоб встановити пароль. Далі вводимо "0" для низькорівневого пароля.

Створюємо пароль. Повторно вводимо пароль та натискаємо "y".

Тепер налаштування завершено.

**Крок 5:** Для початку роботи з MySQL вводимо : 
```sh
sudo mysql -u root
```
Та створюємо нашу першу базу даних:
```sh
CREATE DATABASE gregs_list;
SHOW DATABASES;
USE gregs_list;
```
![](https://github.com/bwaah1/DBMS/blob/main/lab_1/image.png)


## Інсталяція Apache Cassandra на Linux Ubuntu

**Крок 1:** Переконуємося, що Java встановлена :
```sh
java --version
```
**Крок 2:** Додайємо репозиторій Cassandra до файлу cassandra.sources.list. Остання основна версія - 4.0 :
```sh
echo "deb https://debian.cassandra.apache.org 41x main" | sudo tee -a /etc/apt/sources.list.d/cassandra.sources.list deb https://debian.cassandra.apache.org 41x main
```

**Крок 3:** Додаємо ключі сховища Apache Cassandra до списку довірених ключів на сервері :
```sh
$ curl https://downloads.apache.org/cassandra/KEYS | sudo apt-key add -
```

**Крок 4:** Оновлюємо індекс пакунків з джерел:
```sh
sudo apt-get update
```

**Крок 5:** Встановлюємо Cassandra за допомогою APT:
```sh
sudo apt-get install cassandra
```

**Крок 6:** Перевіряємо статус Cassandra та під'єднюємося до СУБД:
```sh
cqlsh
```
![](https://github.com/bwaah1/DBMS/blob/main/lab_1/image2.png)
