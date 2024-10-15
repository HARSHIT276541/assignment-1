


#include <stdio.h>

// Function to convert decimal to binary
void decimal_to_binary(int num) {
    int binary[32];
    int i = 0;
    while (num > 0) {
        binary[i++] = num % 2;
        num = num / 2;
    }
    printf("Binary: ");
    for (int j = i - 1; j >= 0; j--) {
        printf("%d", binary[j]);
    }
    printf("\n");
}

// Function to convert decimal to hexadecimal
void decimal_to_hexadecimal(int num) {
    printf("Hexadecimal: %x\n", num);
}

// Function to convert decimal to octal
void decimal_to_octal(int num) {
    printf("Octal: %o\n", num);
}

int main() {
    int decimal_num;
    printf("Enter a decimal number: ");
    scanf("%d", &decimal_num);

    printf("Decimal: %d\n", decimal_num);
    decimal_to_binary(decimal_num);
    decimal_to_hexadecimal(decimal_num);
    decimal_to_octal(decimal_num);

    return 0;
}

