
# We are writing our first program to sum the first 10 numbers 

### code part you can copy sum.c file
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
riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum.o sum.c
```
```
- or 32 bits
riscv64-unknown-elf-gcc -O0 -mabi=ilp32 -march=rv32i -o lab_1.o lab_1.c
```

- As shown below
<img width="1113" height="98" alt="image" src="https://github.com/user-attachments/assets/1d91a221-a1d3-4517-b48c-291c10f6b9d3" />
Figure shows how to run the above command on terminal

- To run the compiled output we cannot simple run like we did in gcc a.out file.
  
<img width="1115" height="202" alt="image" src="https://github.com/user-attachments/assets/7900cbad-53e2-4b73-b2ca-a60897485505" />

- So what to do we will use spike.  Here probably we cannot see the input we type so dont worry, just type a number and you will get the answer properly. I typed number 2.

<img width="546" height="70" alt="image" src="https://github.com/user-attachments/assets/ea43c8d4-8c5b-49ad-985f-d160d3ce1755" />

### Steps to check the assembly and understand the RISCV code.
- Now open a new terminal & use the command to see the disassembled asembly code
```
riscv64-unknown-elf-objdump -d sum.o
```
- You will observe a very long disassembled code seems very tough to decode what we wrote.
- So we will try with Pipe '| less' command

```
riscv64-unknown-elf-objdump -d sum.o | less
```
- You will see a ":" sign where we can write 

<img width="921" height="212" alt="image" src="https://github.com/user-attachments/assets/bfbd52bd-830c-4357-afed-c360f3ffe9ff" />

- Now type '\main' and press letter "n" As shown in figure below

<img width="1115" height="749" alt="image" src="https://github.com/user-attachments/assets/c53fee75-3e0f-4a5f-8f92-c89f19e5c430" />

- You will press "n" twice you will get main function as shown in figure below

<img width="806" height="747" alt="image" src="https://github.com/user-attachments/assets/a301c9c9-7ac3-43df-b0d5-7e64d140ed2d" />

## Count the Number of Instructions in Main program
- While subtracting use HEX number system and then divide by 4 as Byte addressing.
- You will get total instructions around 26

<img width="763" height="639" alt="image" src="https://github.com/user-attachments/assets/fdabc2c7-7c52-4ed1-a210-2f56cfa4486c" />










