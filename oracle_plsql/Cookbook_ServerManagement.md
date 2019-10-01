**Get Status of server listeners**

    execute the command 

    lsnrctl status


**Allow all ips to connect to the oracle server**

    To manage outside connections to the oracle server, the listerner.ora file in C:\oraclexe\app\oracle\product\10.2.0\server\NETWORK\ADMIN

    must be changed

    LISTENER =
    (DESCRIPTION_LIST =
        (DESCRIPTION =
        (ADDRESS = (PROTOCOL = IPC)(KEY = EXTPROC_FOR_XE))
        (ADDRESS = (PROTOCOL = TCP)(HOST = 0.0.0.0)(PORT = 1521))
        )
    )

    the 0.0.0.0 allows all outside ips to connect to the server in the port 1521


**Monitor Sessions to DB**

    You can monitor the current active sessions to the server listerner by using sqldeveloper Tools-> Monitor Sessions.


    Show all Connections to DB including Inactive

    SELECT * from V$SESSION;


