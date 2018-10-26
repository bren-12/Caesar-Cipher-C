#include <stdio.h>
#include <cs50.h>
#include <string.h>
#include <stdlib.h>
#include <ctype.h>

int main(int argc, char *argv[])
{
    if(argc != 2)
    {
        printf("ERROR: Please enter 1 arguement\n");
        return(1);
    }
    else
    {
        int n = atoi(argv[1]);
        while(n <= 0)
        {
            printf("Invalid Number entered: %i\nTry Again: ", n);
            n = get_int();
        }
    }

    int n = atoi(argv[1]);

    //Takes word in from parameter
    //string word = argv[1];
    printf("plaintext: ");
    string word = get_string();
    printf("Word entered: %s\n", word);
    int wrdlen= strlen(word);
    //Print word length for testing
    //printf("Word length: %i\n", wrdlen);
    char letter;

    //Capitalize test
    //word[0]=toupper(word[0]);
    //printf("CapWord: %s\n", word);

    int cshift = n;
    int i;
    //Loops through each leter in word
    for (i = 0; i < wrdlen; i++)
    {
        //take letter and changes to ascii int
        int c = word[i];

        //checks if c is a capital letter
        if(c >= 65 && c <= 90 )
        {
            //checks to see if adding shift overflows outside cap letter range
            if( c + cshift > 90 )
            {
                int cshift2 = c + cshift;
                cshift2 = cshift2 - 26;
                word[i] = cshift2;
            }
            else
            {
                word[i] = c + cshift;
            }
        }

        //checks if c is a lowercase letter
        if(c >= 97 && c <= 122 )
        {
            //checks to see if adding shift overflows outside cap letter range
            if( c + cshift > 122 )
            {
                int cshift2 = c + cshift;
                cshift2 = cshift2 - 26;
                word[i] = cshift2;
            }
            else
            {
                word[i] = c + cshift;
            }
        }
        // TEST shift ascii int by cipher amount and adds back to string
        /*
        else
        {
            word[i] = c + cshift;
        }
        */
        //printf("Letter: %c\n", word[i]);
       // printf("Ciphertext: %s\n", word);
    }
    printf("Ciphertext: %s\n", word);
    return(0);
}
