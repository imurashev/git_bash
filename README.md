## Working with Git and Bash
Completed the following tasks on writing basic Bash commands:

### Task 1:
| Task | Command |
|--------|----------|
Open the home directory via the terminal|cd /c/Users/Elijah/Desktop/bash_training
Display the name of the current directory|pwd
Create a directory test1 inside this folder|mkdir test1
Navigate to the test1 folder|cd test1
Create files named 1, 2, and 3 inside the test1 directory|touch 1 2 3
Check the contents of the test1 directory|ls
Navigate to the home directory|cd ..
Create a directory test2 inside the home directory|mkdir test2
Delete the test2 directory|rmdir test2
Delete the file 2 from the test1 directory|rm test1/2
Create a directory named test3 in the home directory and add two files to it|mkdir test3; touch test3/11 test3/22
Delete the test3 directory|rm -r test3
Create a directory named test4 in the home directory|mkdir test4
Move files 1 and 3 from test1 to the test4 directory|mv test1/1 test1/3 test4
Add three lines containing the word 'line' to file 1|echo line > test4/1; echo line>> test4/1; echo line>> test4/1
View the contents of file 1|cat test4/1
Add three lines containing the word 'line' to file 3|echo -e "line\nline\nline" >> test4/3
View the contents of both files 1 and 3 at the same time|cat test4/1 test4/3
Using a text editor, replace all lines in file 1|nano test4/1 (without editor: echo -e "text\ntext\ntext" > test4/1)

### Task 2:
| Task | Command |
|--------|----------|
Open the home directory via the terminal|cd /c/Users/Elijah/Desktop/bash_training
Create a directory test3|mkdir test3
Add three files named 4, 5, and 6 to the test3 directory, each containing four lines: row1, row2, row3, row4|echo -e "row1\nrow2\nrow3\nrow4" > test3/4; echo -e "row1\nrow2\nrow3\nrow4" > test3/5; echo -e "row1\nrow2\nrow3\nrow4" > test3/6
Find the line row2 in file 5|grep "row2" test3/5
Find the line containing row in the test3 directory|grep "row" test3/*
Count how many lines containing row are in file 6|grep -c "row" test3/6
Find file 5 inside the test3 directory|find test3 -name "5"
Use the find command to delete file 5|find test3 -name "5" -delete
Use the echo command to add the word test to file 4, overwriting its existing content|echo "test" > test3/4
Replace the word test with fail in file 4|echo "fail" > test3/4
Append the word test to file 4 without overwriting its existing content|echo "test" >> test3/4
View all processes running on the system for all users, not limited to the console|ps aux
Terminate process 666 in the console (you can just write the command without actually killing it)|kill 666
Check the availability of rusau.net using ping|ping rusau.net
Send 5 packets to rusau.net|ping -n 5 rusau.net
Using GET and curl, retrieve information about registered pets with any status from https://petstore.swagger.io/|`curl https://petstore.swagger.io/v2/pet/findByStatus?status=available&status=pending&status=sold`
Using POST and curl, create a new user on https://petstore.swagger.io/|`curl -X POST https://petstore.swagger.io/v2/user -H "Content-Type: application/json" -d "{\"id\": 999009, \"username\": \"user_name999\", \"firstName\": \"John\", \"lastName\": \"Doe\", \"email\": \"exampl@exampl.com\", \"password\": \"secret123\", \"phone\": \"+79011234767\", \"userStatus\": 1}"`
