# **baby-CPP**



- Above is the first block of the assembly program given that is accessing the Command-line Arguments and storing them in (rbp-0x14) and (rbp-0x20).

- We should know that when we put Command-line Arguments then we have to input a vector having its first argument as the name of the executable file and then all the arguments we want to give.

**This gives us our first statement:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/e076506f-6fc3-4de7-a93b-4fef12a4cd08)


**Now we shall see the (block 1) of the assembly:**

- We compare the first argument of the Command-Line Vector := argc to 2 or we simply check if there are 2 arguments given to the command line.

- If the arguments are not 2 then ->

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/9cf8056f-7d61-417d-8786-a7adc53329a8)


- The first two statements describes that "USAGE: ./grade n" has to be printed as an error output statement.

- Also the exit() function is called with EDI equal to 2.

**Thus our code becomes:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/0c93e4a9-2426-4b5f-983b-565e9c4067ad)


- If the argument count is not 2 then we will jump to block 2 :

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/c227cc9d-193c-401c-bd4a-7fa4db400eae)


- Here we can easily observe that the program is converting 1st index argument of the vector (argv) to an integer using 'atoi()' function and storing it inside a variable on the stack.

- Then another variable on the stack is set to 1, at the 7th line of the block.

- Also here we compare the converted number variable (num) to 0 and if it is less or equal to 0, then we move onto the next block (block 3).

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/eeca9ec4-22f5-4577-9d51-ac38ec4499ec)


- This block prints the string "Don't be so negative." as an error output. Also it uses endl after that.

- Then it exits the program using the argument 2 in the RDI register.

**Thus our code becomes:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/b4bb8040-df75-4c5f-a065-c0a22aa4af1b)


**Now we move onto the next block (block 4)**

- We will move here only if num variable is not equal to 0->

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/83b71afb-cf10-4ebb-b992-f87a33fdca10)


- In this block the program is using 'sqrt()' function to evaluate the sqaure root of the 'num' variable value and store it into the variable that I named cnt.

**Thus we got our statement to add:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/b09ff030-172f-4f42-a3fa-cf180a7ca9e5)


**Now the next block is:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/914a17b6-a3ff-49cf-b4f2-1ac9a1eae89d)


- This tells us that the program compares the value stored at (rbp-8) in  the stack or one of the variable with 1.

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/06cb7dfb-8cce-4ec0-b020-f2c48defb9e4)


- Also we can infer that this above can be said a while loop until cnt variable is more than 1 as then only it will get oht of the loop and go to block9.

**Thus our code becomes:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/0ecb8c75-2a2b-4ffe-9496-c8d1017207cf)

- This happens because we will see in the next block sections(block6 and block7) we can transform the calculations into the given code.

- Now let us break out of the loop or simply say set 'cnt' variable to less than or equal to 1.

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/0bfc5ce8-2130-441d-99b0-86aba487f5d1)


- These instructions tell us that we will jump to block11 if 'num' variable is not equal to 1.

- If not then this block will execute:

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/e432359f-626a-4ccf-abe5-b2e0ef9c2107)


**Making our code:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/5e420d1b-2902-4238-ab67-a7c40468fe19)


- The correct if statement if fulfilled then the block10 will be executed making our code giving us the if statement.

### **THUS OUR FINAL CODE IS:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/5487c4b4-1f16-4031-970f-6ad3e7798d77)










