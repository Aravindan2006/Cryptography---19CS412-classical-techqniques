
# EX NO :01 CEASER CIPHER:

## AIM : 

To implement the simple substitution technique named Caesar cipher using C
language.


## ALGORITHM :

Step 1 : Read the plain text from the user.

Step 2 : Read the key value from the user

Step 3 :If the key is positive then encrypt the text by adding the key with
each character in the plain text

Step 4 :Else subtract the key from the plain text.

Step 5 :Display the cipher text obtained above.


## PROGRAM : 

```
#include<stdio.h>
#include <string.h>
#include<conio.h>
#include <ctype.h>
int main()
{
char plain[10], cipher[10];
int key,i,length;
int result;
printf("\n Enter the plain text:");
scanf("%s", plain);
printf("\n Enter the key value:");
scanf("%d", &key);
printf("\n \n \t PLAIN TEXt: %s",plain);
printf("\n \n \t ENCRYPTED TEXT: ");
for(i = 0, length = strlen(plain); i < length; i++)
{
cipher[i]=plain[i] + key;
if (isupper(plain[i]) && (cipher[i] > 'Z'))
cipher[i] = cipher[i] - 26;
if (islower(plain[i]) && (cipher[i] > 'z'))
cipher[i] = cipher[i] - 26;
printf("%c", cipher[i]);
}
printf("\n \n \t AFTER DECRYPTION : ");
for(i=0;i<length;i++)
{
plain[i]=cipher[i]-key;
if(isupper(cipher[i])&&(plain[i]<'A'))
plain[i]=plain[i]+26;
if(islower(cipher[i])&&(plain[i]<'a'))
plain[i]=plain[i]+26;
printf("%c",plain[i]);
}
return 0;
}
```
## OUTPUT :

![image](https://github.com/user-attachments/assets/e829c060-4a28-4ad5-b6ce-3f5b104cc50b)


## RESULT : 

Thus the implementation of Caesar cipher had been executed successfully








