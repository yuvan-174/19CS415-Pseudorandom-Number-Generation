# 19CS415-Pseudorandom-Number-Generation
## AIM:
To implement the Pseudorandom Number Generator Using C.
## Algorithm:
1.  Define constants for the LCG formula (multiplier, increment, and modulus).
2.  Design an lcg() function that takes the seed, applies the LCG formula, and returns the new seed.
3.  In the main function, prompt the user for a seed and number of random numbers to generate.
4.  Use a loop to generate and print the random numbers by repeatedly updating the seed using lcg().
5.  Test with different seed values to ensure correct pseudorandom number generation.
## PROGRAM:
```c
#include <stdio.h>
//Constants for LCG
#define A 1664525
#define C 1013904223
#define M 4294967296 // 2^32

//Linear Congruential Generator function
unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M;
}

int main() {
    unsigned int seed;
    int n, i;
    printf("*Pseudorandom number generator*\n\n");
    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("Random numbers:\n");
    for (i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }
    return 0;
}
```
## OUTPUT:
![Screenshot 2024-10-10 090428](https://github.com/user-attachments/assets/477d2036-35eb-41f3-bf3d-4dce331e710f)

## RESULT:
Thus the Pseudorandom Number Generator is successfully implemented.
