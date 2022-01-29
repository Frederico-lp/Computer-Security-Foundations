# Trabalho realizado na Semana #8 e #9
# LOGBOOK 8 / 9

## Indíce
- Task 1
  
- Task 2.1
  
- Task 2.2
  
- Task 2.3

- Task 3.1

- Task 3.2

# Task 1
For this first task we only needed to run an SQL query to select the tuple where name was Alice.

![aliceSql](/outputs/log8/aliceInfo.png)

# Task 2.1
We started by inputing _" ' or 1=1 -- "_ in username and an irrelevant (since it would be ignored)password in password. This was enough for us to be able to Login, but only as Alice and since our objective was to Login as Admin we needed to try a different approach.

![aliceProfile](/outputs/log8/AliceProfile.png)

We achieved this by changing the previous command to _"Admin ' and 1=1 -- "_, which gave us access to administrator privileges.

![adminHome](/outputs/log8/adminHome.png)
![adminProfile](/outputs/log8/adminProfile.png)

# Task 2.2
In this task we used the same input as in the task before but this time we replaced _white spaces_ for _%20_ and _'_ for _%27_, which resulted in the following:

_username=Admin%20%27%20and%201=1%20--%20_

![adminhtml](/outputs/log8/curlLogin.png)

To see the full HTML code, please go to the _outputs/log8/admin.html_ file.

# Task 2.3
Due to the fact that de code is not evaluating the SQL statement if there is several statements, to update the table you first need to login, then you can run the SQL statement to change tables.

This can be countermeasured by using SQL variables, that independently of the input statement, can filter what values are wanted and those who are not.

# Task 3.1
We started by logging in on Alice's page with the previously used command (_' or 1=1 --_).

After that, and taking in account the expected SQL statement, we ran _ok',salary='99999_ which changed Alice's salary to 99999.

![adminhtml](/outputs/log8/aliceSalary.png)

# Task 3.2
We need to end the changing salary query (previous task) with _WHERE name='Boby';#_. That way we can change Bobby's salary: ok',salary='99999' WHERE name='Boby';#

![bobySalary](/outputs/log8/bobySalary.png)


# CTFs
## Desafio 1:
- As the analysis from the source code revealed a weakness in the processing of the SQL statements, we used that weakness (processing of " and ' on the SQL statement) to log in as admin and get the flag.

## Desafio 2:
- After pinging a server and experimenting with the pinging page, we realized that if we insert && after the server we can run linux command line statements, so we pinged a server and printed the flag using 8.8.8.8 && cat /flag.txt