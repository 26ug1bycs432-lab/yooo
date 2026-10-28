# Sum of Two Numbers

This C program reads two integers, adds them, and prints their sum.

## How it works

1. `#include <stdio.h>` makes `printf` and `scanf` available.
2. `main` declares two integer variables, `first` and `second`.
3. `scanf` reads two integers. It returns how many values it successfully read; if that is not `2`, the program exits with an error status.
4. The program adds the values and prints the result.

## Refactored code

```c
#include <stdio.h>

int main(void) {
    int first;
    int second;

    printf("Enter two numbers: ");
    if (scanf("%d %d", &first, &second) != 2) {
        fprintf(stderr, "Please enter two valid integers.\n");
        return 1;
    }

    printf("Sum: %d\n", first + second);
    return 0;
}
```

The refactoring keeps the program's behavior but makes the input variables explicit and reports invalid input to the error stream.