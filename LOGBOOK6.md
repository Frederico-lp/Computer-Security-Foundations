# Trabalho realizado na Semana #6
# LOGBOOK 6

## Indíce
- Task 1
  
- Task 2.A
  
- Task 2.B
  
- Task 3.A

- Task 3.B

# Task 1
In this task we reidirected output to a file using "printf '%d' {1..1600} >> payload.txt" and then sent this file do the server as input. We verified that the program crashed and myprintf didn't return since there were no prints in the server terminal

![server_output](/outputs/log6/log6_task1_1.PNG)
![client_output](/outputs/log6/log6_task1_2.PNG)

# Task 2
## Task 2.A
In this task we created a file with "A"s in the beggining, followed by many %x to print out program stack. After 63 '%x', the ASCII of A was finally printed out. This means that after 63's %x the server starts to print out the content of the memory addresses in which our input was saved. This result will be used in the next tasks.

![server_output2](/outputs/log6/Screenshot3.png)

## Task 2.B
For this problem we used the result given in the previous program. We started by inputing the memory address of the secret message and then used 63 '%x' followed by '%s' to print the  content of the address we inputed in the beggining.


![python_script](/outputs/log6/pythonScriptMessage.png)
![server_output3](/outputs/log6/ServerSecretMessage.png)

# Task 3
## Task 3.A
In this task we did something similar to what was done in task 2.B with the difference that this time we used %n instead of %s. %n is used to write the number of bytes written before it. In this case since we had 63's %x that wrote 8 bytes each, %n writes 63*8 in hexadecimal.

![python_script](/outputs/log6/scriptforchange.png)
![server_output4](/outputs/log6/changeValue.png)

## Task 3.B
For this final task we had to do something similar to what was done in 3.B but this time %n had to write 0x5000. For this we used 62's %x to get to the right position and in the last %x we specified how long will the be the bytes read. 0x5000 - (62*8 + 4) is the number represented by 0x5000 (the number we want %n to write) minus 62*8 (62's %x that write 8 bytes) + 4 (the bytes of the address written in the beggining). After this %n writed 0x5000 as expected.

![python_script](/outputs/log6/scriptMessage.png)
![server_output4](/outputs/log6/changingMessage.png)

