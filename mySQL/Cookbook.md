**Show all users**

    select Host, User from mysql.user;



**Create An User**

    CREATE USER 'hbstudent'@'%' IDENTIFIED BY 'hbstudent';
    GRANT ALL PRIVILEGES ON * . * TO 'hbstudent'@'%';
    ALTER USER 'hbstudent'@'%' IDENTIFIED WITH mysql_native_password BY 'hbstudent';

    The % allows the user to connect from any host. This is important for creating users when running mysql server in a container and you want to allow the user to connect from outside of the container


**Test JDBC Connection**

    public class App 
    {
        private static final String MY_SQL_JDBC_URL = "jdbc:mysql://localhost:3306/hb_student_tracker?useSSL=false&serverTimezoneUTC&allowPublicKeyRetrieval=true";
        private static final String USER = "hbstudent";
        private static final String PASS = "hbstudent";
        
        public static void main( String[] args ) throws SQLException
        {
            System.out.println("Connecting to database: " + MY_SQL_JDBC_URL);
            Connection myConnection = DriverManager.getConnection(MY_SQL_JDBC_URL , USER , PASS);
            System.out.println("Connection success");
        }
    }


**Show the Structure of a Entity**

    mysql> desc something;

    (for example desc table_name;)



**Run script in the command line**

    mysql -h 127.0.0.1 -P 3306 -u root -p < create-db.sql



**Show All Databases**

    show databases;


