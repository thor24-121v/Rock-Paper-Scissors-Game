# Rock-Paper-Scissors-Game
Play this rock paper scissors game and remember your childhood days


#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
    int i, random, round, computer_score, user_score;

    char computer_choose, user_choose;

    srand(time(0));
    random = rand() % 100;

    if (random <= 33 && random >= 0)
    {

        computer_choose = 's';
    }
    if (random > 33 && random <= 66)
    {

        computer_choose = 'p';
    }

    if (random > 66 && random <= 100)
    {

        computer_choose = 'r';
    }

    printf("Choose S for SCISSORS\nChoose R for Rock and\nChoose P for PAPER\n\n");
    printf("Enter Your Choice : \n");
    scanf("%c", &user_choose);

    //   printf("Computer Choose  %c\n", computer_choose);

    if (computer_choose == 's' && user_choose == 'p')
    {
        printf("Computer Choose %c and\nUser Choose %c\n", computer_choose, user_choose);
        printf("Computer Won\n");

        computer_score = 1;
        user_score = 0;
    }

    else if (computer_choose == 's' && user_choose == 'r')
    {
        printf("Computer Choose %c and\nUser Choose %c\n", computer_choose, user_choose);
        printf("User Won\n");

        user_score = 1;
        computer_score = 0;
    }

    else if (computer_choose == 's' && user_choose == 's')
    {
        printf("Computer Choose %c and\nUser Choose %c\n", computer_choose, user_choose);
        printf("Match Draw\n");

        user_score = 1;
        computer_score = 1;
    }

    else if (computer_choose == 'r' && user_choose == 's')
    {
        printf("Computer Choose %c and\nUser Choose %c\n", computer_choose, user_choose);
        printf("Computer Won\n");

        computer_score = 1;
        user_score = 0;
    }

    else if (computer_choose == 'r' && user_choose == 'p')
    {
        printf("Computer Choose %c and\nUser Choose %c\n", computer_choose, user_choose);
        printf("User Won\n");

        computer_score = 0;
        user_score = 1;
    }

    else if (computer_choose == 'r' && user_choose == 'r')
    {
        printf("Computer Choose %c and\nUser Choose %c\n", computer_choose, user_choose);
        printf("Match Draw\n");

        computer_score = 1;
        user_score = 1;
    }

    else if (computer_choose == 'p' && user_choose == 'r')
    {
        printf("Computer Choose %c and\nUser Choose %c\n", computer_choose, user_choose);
        printf("Computer Won\n");

        computer_score = 1;
        user_score = 0;
    }

    else if (computer_choose == 'p' && user_choose == 's')
    {
        printf("Computer Choose %c and\nUser Choose %c\n", computer_choose, user_choose);
        printf("User Won\n");

        computer_score = 0;
        user_score = 1;
    }

    else if (computer_choose == 'p' && user_choose == 'p')
    {
        printf("Computer Choose %c and\nUser Choose %c\n", computer_choose, user_choose);
        printf("Match Draw\n");

        computer_score = 1;
        user_score = 1;
    }
}
