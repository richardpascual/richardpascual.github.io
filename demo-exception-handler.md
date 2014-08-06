---
title: demo-exception-handler
layout: post
---

# Sample Work for _richpascual_

## Oracle PL/SQL Exception Handler

This is a sample Oracle PL/SQL stored procedure with two insert statements against some demo tables that have typical constraints such as unique/primary key columns.  The tables are from a larger schema featured on the [uglysql project](http://github.com/richardpascual/uglysql) called the "DOJ Crime Report" schema.  Otherwise, just create your own (probably simpler) tables with data and constraints that can report some sort of ora exception report. 


        CREATE OR REPLACE PROCEDURE DOJ_ERROR_TEST_INPUT 
		IS
        
		BEGIN

        -- Test Error # 1:  The Person's Name Cannot be Null
   
        -- This one is OK:<br>
        INSERT INTO DOJ_PERSON ( PERSON_ID, PERSON_NAME, DATE_OF_BIRTH, DATE_ADDED, DATE_MODIFIED )
        VALUES ( null, 'RICK GRIMES', to_date('15-AUG-1995','DD-MON-YYYY'), sysdate, null);
        COMMIT;

        dbms_output.put_line('Sheriff Rick Grimes added for duty.');

        -- This one is NOT: (note, I am forcing re-use of a sequenced ID that is supposed to be 
		-- unique for all records)
        INSERT INTO DOJ_PERSON ( PERSON_ID, PERSON_NAME, DATE_OF_BIRTH, DATE_ADDED, DATE_MODIFIED )
        VALUES ( 1, 'ROSCOE PICO', to_date('15-AUG-1995','DD-MON-YYYY'), sysdate, null);
        COMMIT;

        EXCEPTION
           WHEN Others THEN
              err.handle ( detail => 'DOJ_ERROR_TEST_INPUT',
			                 info => 'Test demo for my 1.0 version release.' );

        END;


To run the procedure:

        BEGIN
           DOJ_ERROR_TEST_INPUT();
        END;

		
		
        Sheriff Rick Grimes added for duty.

        Statement processed.


        0.09 seconds

		
To check the output to the exception log:		
		
        select * from errlog;
		
		
<div align="center">![[images/errlog-simple-output.jpg]]</div>		


This is what the output of the table content looks like, showing the exception thrown and also recording the two optional text fields specified by the package design.  These fields work well for self-identification, so that the object that fails has a way of naming itself when the exception log is populated.
		



        		
		
