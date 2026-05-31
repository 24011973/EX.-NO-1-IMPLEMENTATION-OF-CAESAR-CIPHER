# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>

int main() {
    char plainText[100];
    int key, i = 0;
    printf("Enter the plain text: ");
    fgets(plainText, sizeof(plainText), stdin);
    printf("Enter the key (positive or negative): ");
    scanf("%d", &key);

    while (plainText[i] != '\0' && plainText[i] != '\n') {
        char ch = plainText[i];
        
   
        if (ch >= 'A' && ch <= 'Z') {
          
            if (key >= 0)
                ch = (ch - 'A' + key) % 26 + 'A';
            else
                ch = (ch - 'A' + 26 + key) % 26 + 'A';
        } else if (ch >= 'a' && ch <= 'z') {
           
            if (key >= 0)
                ch = (ch - 'a' + key) % 26 + 'a';
            else
                ch = (ch - 'a' + 26 + key) % 26 + 'a';
        }
        
        plainText[i] = ch;
        i++;
    }
    printf("Cipher text: %s\n", plainText);
    return 0;
}


```

## OUTPUT:

<img width="1918" height="990" alt="image" src="https://github.com/user-attachments/assets/d0db440b-8aa1-46cb-8fe2-e9556164bdde" />

<img width="1915" height="968" alt="image" src="https://github.com/user-attachments/assets/da1cc0c3-49e9-46ed-ae9b-a7ac1340a343" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
