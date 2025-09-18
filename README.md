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
#include <string.h>
void caesarCipher (char *text, int shift)
{
for (int i = 0; text[i]; i++)
{
if (text[i] >= 'A' && text[i] <= 'Z')
text[i] = ((text[i] 'A' + shift + 26) % 26) + 'A';
else if (text[i] >= 'a' && text[i] <= 'z')
text[i] = ((text[i] 'a' + shift + 26) % 26) + 'a';
}
}
int main()
{
char text[100];
int shift;
printf("Enter text: ");
fgets(text, sizeof(text), stdin);
text[strcspn(text, "\n")] = 0;
printf("Enter shift value: ");
scanf("%d", &shift);
caesarCipher (text, shift);
printf("Encrypted Message: %s\n", text);
caesarCipher (text, shift);
printf("Decrypted Message: %s\n", text);
return 0;
}
```
## OUTPUT:
<img width="908" height="567" alt="image" src="https://github.com/user-attachments/assets/79f3408f-2e56-4e2d-ab6c-2092b8b1fe8b" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
