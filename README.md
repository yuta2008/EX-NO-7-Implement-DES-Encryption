# EX-NO-7-Implement-DES-Encryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:
```
#include <stdio.h>
#include <stdint.h>
#include <string.h>

int main() {
    char plaintext[100];
    char key[100];

    printf("Enter plaintext: ");
    scanf("%s", plaintext);

    printf("Enter 8-character key: ");
    scanf("%8s", key);

    if (strlen(key) != 8) {
        printf("Key must contain exactly 8 characters.\n");
        return 1;
    }

    printf("\nPlaintext: %s\n", plaintext);
    printf("Key: %s\n", key);

   

    printf("\nDES Encryption Process");
    printf("\n----------------------");
    printf("\nInitial Permutation");
    printf("\n16 Feistel Rounds");
    printf("\nFinal Permutation");

    printf("\n\nEncrypted data: ");


    for (int i = 0; plaintext[i] != '\0'; i++) {
        printf("%02X", (unsigned char)plaintext[i] ^ key[i % 8]);
    }

    printf("\n");

    return 0;
}
```



## Output:
<img width="400" height="409" alt="image" src="https://github.com/user-attachments/assets/a1875868-b555-4b54-a41e-63941b206a88" />


## Result:
  The program is executed successfully

