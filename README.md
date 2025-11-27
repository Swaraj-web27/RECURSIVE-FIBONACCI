# RECURSIVE-FIBONACCI
#include <stdio.h>
int fibonacci(int *n) {
    if (*n == 0)
    return 0;
    if (*n == 1)
    return 1;
    int a = *n - 1;
    int b = *n - 2;
    return fibonacci(&a) + fibonacci(&b);
    }
int main() {
    int i, n;
    printf("Enter number of terms: ");
    scanf("%d", &n);
    printf("Fibonacci Series up to %d terms:\n", n);
    for (i = 0; i < n; i++) {
        int x = i;
        printf("%d ", fibonacci(&x));
    }
    return 0;
}
