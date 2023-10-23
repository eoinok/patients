# Week 6 Lab

Clone this repo into your www folder under laragon. In the command prompt cd into the \laragon\www folder. Make sure that you are in the correct folder and that laragon\www appears in the command prompt. Type git clone your-repo-url (Get your repo url from github after creating the repo). Then cd into the folder you have just cloned by typing cd week6Lab-yourgithubid. Once you are in the correct folder, keep this command window open so you can type in your git commands as required.

This lab further builds on your ability to connect PHP to a MySQL database and process data into and out of the database. By the end of this lab students will be able to:

Gather data from a form and insert it into a database

# Part 1
Copy and paste the SQL script from the patients.sql file in the starter code from the assignment. Place it in a new query window in HeidiSQL. Execute the query so that a new database will be created complete with three tables Patient, Doctor and Visit. Note which table has Foreign Keys.

Given the form you have been given in the starter code called createNewVisit.html, write a PHP program which will gather data from the form and insert it into the patients database. In order to do this you must figure out what to call your new file. This can be determined from the action attribute of the FORM tag in the createNewVisit.html file.
Your new PHP program should contain an include command which pulls in PHP code containing credentials to connect to the patients database. You can call this file dbcon.php and you may reuse code you have written in previous labs but remember the database name will be different.

The program should then pull values from the form and assign them to simple SQL attributes. Once all the values from the form have been assigned to simple SQL attributes they can be used to build a simple SQL "insert into" statement. To do this take one of the INSERT INTO statements from the patients.sql file, enclose this in quotation marks and assign it to a PHP varaible called $sql. 
Modify this Insert into statement so that rather than using hard-coded data, it uses values from the simple PHP variables that contain the values from the HTML FORM.

echo your $sql variable to the screen. Test your code. If the sql statement on the screen looks correct, than copy and paste it into HeidiSQL into a new query window. Verify that it works by executing your query. If the syntax of your SQL is correct a new row should be created in the Visit table. Once you have ensured that the SQL statement is correct, commit and push your code.

# Part 2









Change the action on the form so that when the Submit button is pushed the form data will be submitted to a PHP file called createNewBooking.php.
Add two input boxes to the HTML form one which gets the member's ID for the booking and a second which gets the court ID make sure these input boxes use the names memberID and courtID respectively. Note the capitalisation on these names.
Modify the createBooking.php file so that it contains an include statement that pulls in code from a file called dbcon.php. This file should contain your database credentials. When you have completed these changes try to create a new tennisclub booking using your form - visit http://localhost/week5lab-yourgithubid/newBooking.html. Use memberID = 2 and courtID = 3. This will output some SQL code to the screen. If the code looks correct, comment out the line in createNewBooking.php that echoes the screen and uncomment the subsequent block of code which executes the SQL command against the connection to the database. Try submitting your form again, it should say added new record successfully. To see if it worked, type Select * from booking in the HeidiSQL database application. Is your booking there? Try it again with values memberID = 13 and courtID = 15. What happened? Why was this? Write a comment in the PHP code of createNewBooking.php which explains why these numbers don't work. Commit and push your changes.
Part 2

