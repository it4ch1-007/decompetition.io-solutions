# **baby-CPP**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/7311c80c-a73a-40a2-8399-fbca9f6d9e10)



- Above is the first block of the assembly program given that is accessing the Command-line Arguments and storing them in (rbp-0x14) and (rbp-0x20).

- We should know that when we put Command-line Arguments then we have to input a vector having its first argument as the name of the executable file and then all the arguments we want to give.

**This gives us our first statement:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/c92ab3d5-db6c-4d48-a9be-be3ef7873f61)


**Now we shall see the (block 1) of the assembly:**

- We compare the first argument of the Command-Line Vector := argc to 2 or we simply check if there are 2 arguments given to the command line.

- If the arguments are not 2 then ->

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/7941ed41-64aa-445b-9943-c730c4e6da65)



- The first two statements describes that "USAGE: ./grade n" has to be printed as an error output statement.

- Also the exit() function is called with EDI equal to 2.

**Thus our code becomes:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/b688c5e2-fdd1-4e1d-8761-82da2b79e741)



- If the argument count is not 2 then we will jump to block 2 :

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/6db60386-8290-4676-b148-dd9a24e8b3f9)



- Here we can easily observe that the program is converting 1st index argument of the vector (argv) to an integer using 'atoi()' function and storing it inside a variable on the stack.

- Then another variable on the stack is set to 1, at the 7th line of the block.

- Also here we compare the converted number variable (num) to 0 and if it is less or equal to 0, then we move onto the next block (block 3).

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/bd76f626-3b07-4c17-9e46-e716eeaa5ab4)



- This block prints the string "Don't be so negative." as an error output. Also it uses endl after that.

- Then it exits the program using the argument 2 in the RDI register.

**Thus our code becomes:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/19d7dde3-3719-4266-9a14-0f6eb4470df6)



**Now we move onto the next block (block 4)**

- We will move here only if num variable is not equal to 0->

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/7ecf4715-ea85-4828-a8c3-af8492ecbaf4)



- In this block the program is using 'sqrt()' function to evaluate the sqaure root of the 'num' variable value and store it into the variable that I named cnt.

**Thus we got our statement to add:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/269cea6f-37d2-46e1-abd8-8d66cb9e4f12)



**Now the next block is:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/d03bcac3-6822-4aa7-b25a-073330326922)



- This tells us that the program compares the value stored at (rbp-8) in  the stack or one of the variable with 1.

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/614501a1-b9ad-4585-9732-01399f7ffa96)



- Also we can infer that this above can be said a while loop until cnt variable is more than 1 as then only it will get oht of the loop and go to block9.

**Thus our code becomes:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/768e64e9-cc51-4ded-aa65-429ec667cde1)


- This happens because we will see in the next block sections(block6 and block7) we can transform the calculations into the given code.

- Now let us break out of the loop or simply say set 'cnt' variable to less than or equal to 1.

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/0f1d5c1c-9f33-49bf-b2d7-643783965b62)



- These instructions tell us that we will jump to block11 if 'num' variable is not equal to 1.

- If not then this block will execute:

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/9df06725-31c4-47db-a3b4-93306e288b5f)



**Making our code:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/09815c6d-e048-4065-a290-a9c3c3186297)



- The correct if statement if fulfilled then the block10 will be executed making our code giving us the if statement.

### **THUS OUR FINAL CODE IS:**

![image](https://github.com/it4ch1-007/decompetition.io-solutions/assets/133276365/5d1044f8-b425-4eb7-8723-6b90c0f13f52)











