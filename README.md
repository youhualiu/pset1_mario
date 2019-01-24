# pset1_mario
#include<stdio.h>
#include<cs50.h>

void pyramids(int h);
int get_positive_int(string prompt);

int main(void)
{
    int height = get_positive_int("Height: ");
    pyramids(height);
}

void pyramids(int h)
{
    for(int i = 0;i<h;i++)
    {
        int counter = 0;
        int counter2 = 0;
        while(counter < h - i - 1)
        {
            printf(" ");
            counter++;
        }
        
        while(counter >= h - i - 1 && counter < h)
        {
            printf("#");
            counter++;
        }
        printf("  ");
        while(counter2<i+1)
        {
            printf("#");
            counter2++;
        }
        printf("\n");
        
    }
}

int get_positive_int(string prompt)
{
    int n;
    do
    {
        n = get_int("%s",prompt);
    }
    while(n<1);
    return n;
}
