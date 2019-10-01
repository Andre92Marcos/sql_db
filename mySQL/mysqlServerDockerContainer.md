**How to run and connect to a Mysql Server in a docker container**

    docker run --name mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password -d mysql

    mysql -h127.0.0.1 -P 3306 -uroot -p


**Creating Users for a docker container**

    You can create a user the is allowed to connect to any host

    CREATE USER 'hbstudent'@'%' IDENTIFIED BY 'hbstudent';
    GRANT ALL PRIVILEGES ON * . * TO 'hbstudent'@'%';
    ALTER USER 'hbstudent'@'%' IDENTIFIED WITH mysql_native_password BY 'hbstudent';

    Or you must specify the internal container ip. localhost will not work


