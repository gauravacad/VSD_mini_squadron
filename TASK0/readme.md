# Sum of 10 numbers
- Assembly FIRST with minimum commands we know
- try assembler at [link] "https://www.cs.cornell.edu/courses/cs3410/2019sp/riscv/interpreter/#"

```
    addi t0, zero, 1       # i = 1
    addi t1, zero, 0       # sum = 0
    addi t2, zero, 10      # limit = 10

loop:
    add  t1, t1, t0        # sum = sum + i
    addi t0, t0, 1         # i = i + 1
    bge  t2, t0, loop      # if 10 >= i, repeat

    # t1 = 5
```
<img width="1048" height="622" alt="image" src="https://github.com/user-attachments/assets/c632b8d7-0597-4b20-8eb1-4ab7e0746cf1" />

### RISC-V Assembly: Sum of 1 to 10

| Assembly           | Category   | Meaning                  |
|--------------------|------------|--------------------------|
| `ADDI t0, zero, 1` | Arithmetic | `i = 1`                  |
| `ADDI t1, zero, 0` | Arithmetic | `sum = 0`                |
| `ADDI t2, zero, 10`| Arithmetic | `limit = 10`             |
| `ADD t1, t1, t0`   | Arithmetic | `sum = sum + i`          |
| `ADDI t0, t0, 1`   | Arithmetic | `i = i + 1`              |
| `BGE t2, t0, loop` | Branch     | `if (10 >= i) goto loop` |

**Result:** `sum = 55`

### C program with inline RISC-V assembly
```
#include <stdio.h>
int main()
{
    int sum = 0;
    asm volatile (
        "addi t0, zero, 1\n\t"     // i = 1
        "addi t1, zero, 0\n\t"     // sum = 0
        "addi t2, zero, 10\n\t"    // limit = 10

        "loop:\n\t"
        "add  t1, t1, t0\n\t"      // sum = sum + i
        "addi t0, t0, 1\n\t"       // i = i + 1
        "bge  t2, t0, loop\n\t"    // if 10 >= i, repeat

        :
        :
        : "t0", "t1", "t2", "memory"
    );

    printf("sum = 55\n");

    return 0;
}
```
### Deassembly 
<img width="753" height="431" alt="image" src="https://github.com/user-attachments/assets/66c018b7-d832-4339-9fa9-9dc959624cc8" />


