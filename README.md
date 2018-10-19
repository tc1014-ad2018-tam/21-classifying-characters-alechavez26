# 21-classifying-characters-alechavez26
21-classifying-characters-alechavez26 created by GitHub Classroom
/*
 *This program clasiffy each char that are in a string in vowel, consonant.
 *
 * Alejandra Chávez Cruz
 * A01411970@itesm.mx
 * 18/Oct/18
 */
#include <stdio.h>
#include <ctype.h>

int main(void) {
    //Declaration of variables
    char string[100];
    char v;
    int i=0;

    //We tell the user
    printf("Write a text: ");
    fgets(string, sizeof(string),stdin);


    while (string[i]!='\0'){
        if(isalpha(string[i])){
            v=(char)toupper(string[i]);
            if(v=='A'||v=='E'||v=='I'||v=='O'||v=='U'){
                printf("The  character %c is a vowel.\n", string [i]);
            }

                else {
                printf("The character of  %v is a consonant.\n", string[i]);
            }

        }
        else {
            if(isdigit(string[i])){
                printf("The character of  %v is a digit.\n", string[i]);
            }
            else {
                if(isspace(string[i])){ 
                    printf("The character of %v is an space.\n", string[i]);
                }
                else{ 
                    printf("The character of %v is an special character.\n", string[i]);
                }
            }
        }
        ++i;
    }

    return 0;
}
