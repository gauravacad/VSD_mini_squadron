
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

### Steps to RUN
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
