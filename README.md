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
#include <stdio.h>
#include <string.h>

int main() {
    char text[100];
    int key, i;
    
 printf("Enter the plain text: ");
fgets(text, sizeof(text), stdin);
    
text[strcspn(text, "\n")] = 0;

     
 printf("Enter the key value: ");
    scanf("%d", &key);

    
  for (i = 0; text[i] != '\0'; ++i) {
     char ch = text[i];

        
  if (ch >= 'A' && ch <= 'Z') {
            ch = ((ch - 'A') + key) % 26;
            if (ch < 0) ch += 26;
            text[i] = ch + 'A';
        }
        
  else if (ch >= 'a' && ch <= 'z') {
         ch = ((ch - 'a') + key) % 26;
        if (ch < 0) ch += 26; 
        text[i] = ch + 'a';
        }
    }

    
  printf("Encrypted Cipher Text: %s\n", text);

 return 0;
}

## OUTPUT:
<img width="341" height="122" alt="image" src="https://github.com/user-attachments/assets/1b678453-78be-4b8a-9069-d31e1c3a9ab1" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
