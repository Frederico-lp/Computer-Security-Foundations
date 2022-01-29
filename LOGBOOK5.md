# Trabalho realizado na Semana #5
# LOGBOOK 5

## Indíce
- Task 1
  
- Task 2
  
- Task 3

# Task 1

- After compiling and making the program, we ran _a32.out_ and _a64.out_ and both provided us the same outcome, creating a new shell process inside the shell.

# Task 2

- In bof funtion we can see that there is a possible buffer overflow in the "strcpy(buffer, str)" command since BUF_SIZE is set to 100 and str can have a size of 517 ("fread(str, sizeof(char), 517, badfile)").

# Task 3

- On trying to find the buffer address and the value of $ebp by running the commands on the gdb described on the guide, we found that:
![buffer_address](/outputs/log5/log5_task3.png)

- As the difference between $ebp address and buffer address is 108 we decided to use an offset of 108 + 4 = 112

- As the $ebp address is 0xffffcad8 and we were warned that outside the gdb the frame pointer value would be larger we decided to use an arbitrary value for ret but one that is still inside the NOP block, we used 0xffffcb80
![note2](/outputs/log5/log5_task3_2.png)

- As the max size of str we can strcpy from badfile is 517 we decided to write the shellcode (that is 27 bytes long) at 517 - 27 = 490 so it was all contained in str but nearest to the end as possible.

- In the end our exploit.py file was like this and we were able to get a root shell process inside the shell
![exploit](/outputs/log5/log5_task3_3.png)

