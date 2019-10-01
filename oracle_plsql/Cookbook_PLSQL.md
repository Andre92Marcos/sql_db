**Declare Variables**

    DECLARE
        field_order NUMBER := 1;
        v_parentId_reg NUMBER(19);


**Begin and End instructions blocks**

	BEGIN
		[intructions]
	END;

**Iterate through Results of SELECT**

	FOR group_config_id_index IN (select unique PLAYER_REQUIRED_DATA_SET.GROUP_CONFIG_ID FROM PLAYER_REQUIRED_DATA_SET)
	LOOP
	BEGIN
		[instructions]
	END
	END LOOP;

**Assign to Variables**

	field_order := field_order + 1;


**Save state to revert changes if necessary**

    SAVEPOINT do_insert_group_id;
    [instructions]
    ROLLBACK TO do_insert_group_id;

**Catch All Exceptions**

	EXCEPTION
			WHEN OTHERS THEN
				DBSM_OUTPUT.PUT_LINE('Could not migrate ' || group_config_id_index.GROUP_CONFIG_ID);
				ROLLBACK TO do_insert_group_id;

**Cursor**

    DECLARE

        CURSOR <name_of_cursor> IS
            <select>;

    var_name	

        BEGIN
        OPEN <name_of_cursor>
        LOOP
            FETCH  <name_of_cursor> INTO <var_name>
            EXIT WHEN <name_of_cursor>%NOTFOUND
            <can hava mutiple exits when>
            <do stuff with <var_name>>
        END LOOP;
        CLOSE <name_of_cursor>;
    END;


**Prompt User for Input**

    select group_config_id into groupConfigId from tournament_schema.group_config gc where gc.group_id = &group_id;

        prompts user for a group_id

    or for a text value

        '&supplier_name'


**if else**

    IF condition THEN
    {...statements to execute when condition is TRUE...}

    ELSE
    {...statements to execute when condition is FALSE...}

    END IF;

**Compare Strings**

    IF shipment_expedite_hawb = 'PD' THEN

