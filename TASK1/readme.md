
# We are writing our first program to sum the first 10 numbers 

### code part you can copy 
```
#include <stdio.h>
int main(){
	int n, i, sum = 0;
	printf("Enter a positive integer: ");
	scanf("%d", &n);
	for(i=1;i<=n;++i){
		sum += i;
	}
	printf("sum = %d",sum);
	return 0;
}
```

### Steps to ccompile and run the code on gcc complier
- Open the Linux virtual Machine
- Open the terminal
- Make a folder on Desktop using 'mkdir task1' press enter
- Now on prompt change the directory 'cd Desktop/task1'
- Now type 'vim sum.c'
- copy the code from this github link
- go to open file sum.c carefully press insert by pressing 'i'
- File -> paste
- presee esc key
- inset the symbol ':wq' enter
- You will the prompt
- Now write cat sum.c , you will see the code on the terminal
- Press enter and type `gcc sum.c`
- now write ls , you will see a green colour a.out file
- Run a.out file using ./a.out
- you will see the code running.
- Thanks.

### Steps to Compile the code using RISC-V toolchain
```
riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
```
- As shown below
<img width="1113" height="98" alt="image" src="https://github.com/user-attachments/assets/1d91a221-a1d3-4517-b48c-291c10f6b9d3" />
Figure shows how to run the above command on terminal

- To run the compiled output we cannot simple run like we did in gcc a.out file.
  
<img width="1115" height="202" alt="image" src="https://github.com/user-attachments/assets/7900cbad-53e2-4b73-b2ca-a60897485505" />

- So what to do we will use spike.  Here probably we cannot see the input we type so dont worry, just type a number and you will get the answer properly. I typed number 2.

<img width="546" height="70" alt="image" src="https://github.com/user-attachments/assets/ea43c8d4-8c5b-49ad-985f-d160d3ce1755" />

### Steps to check the assembly and understand the code.




