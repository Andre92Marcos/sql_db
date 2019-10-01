**Show all words in the db dictionary**

    select * from dict;


**Find a constraint**

    select * from all_constraints where constraint_name like '%CONSTRAINT_NAME%';

**Show all users**

    select * from dba_users;

    you can also order the users by schema 

    SELECT * FROM dba_users order by DEFAULT_TABLESPACE; 
	

**Show all users that have a specific Role**

    select * from dba_role_privs where granted_role='DBA';

**Get all roles Granted to a user/role**

    select * from USER_ROLE_PRIVS where USERNAME='SAMPLE';
    select * from USER_TAB_PRIVS where Grantee = 'SAMPLE';
    select * from USER_SYS_PRIVS where USERNAME = 'SAMPLE';

