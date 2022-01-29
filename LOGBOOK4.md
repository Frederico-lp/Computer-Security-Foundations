# Trabalho realizado na Semana #4
# LOGBOOK 4

## Indíce
- Task 1
  
- Task 2
  
- Task 3
  
- Task 4

- Task 5

- Task 6

## TASK 1

- The output of Task 1 can be ffound on _task1.txt_ file on the _outputs/lab4_ folder.

## TASK 2

- On the first compilation, we obtained the contents on _task2-output1.txt_ file which is located on the _outputs/lab4_ folder 

- On the second compilation, we obtained the contents on _task2-output2.txt_ file which is located on the _outputs/lab4_ folder 
  
- On comparing the differences between the _task2-output1.txt_ and _task2-output2.txt_ files using the _diff_ command we got nothing, and with that, we can conclude that the child process inherits **all** the parent's environment variables, being the only difference between the two files the output file they were written to.

## TASK 3

- On running the _myenv.c_ file with _NULL_ as the third argument of _execve_ we got nothing. As we changed the third argument of _execve_ to _environ_ we got all the environment variables, concluding that the environment variables **are not** automatically inherited by the new program. The output can be found on _task3-output_ file on the _outputs/lab4_ folder.

## TASK 4  

- We can verify that the environment variables of the new program are passed to _/bin/sh_, the output can be found on _task4-output.txt_ on the _outputs/lab4_ folder.

## TASK 5

- All he environment variables set in the terminal were displayed. That means SET-UID processes inherit the environment from the parent process

## TASK 6

- In this task I added a new directory to the PATH. This new directory had a file called ls.c that was compiled to ls. After this, when I executed the program in task 6 with the "system("ls");" call, it executed my ls instead of the standard ls.
