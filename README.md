## PRADEEP P S
## 212220230034
# <P align='center'>STRING TO NUMBER</P>
## Program:
``` c
#include <stdio.h>
#include<string.h>
#include<stdlib.h>
char *word(char str[],int *i)
{
    char *part=malloc(sizeof(100));
    for(int k=*i,j=0;str[k];k++)
    {
        if(str[k]==' ' || str[k]=='\0')
        break;
        else
        part[j++]=str[k];
        *i=k;
    }
    return part;
}
int check(char w[])
{
    char numbers[12][10]={"zero","one","two","three","four","five","six","seven","eight","nine","double","triple"};
    for(int i=0;i<12;i++)
    {
        if(!strcmp(numbers[i],w))
        return i;
    }
}
int main() 
{
    long int num=0;
    char str[100],w[100][100];
    scanf("%[^\n]",str);
    int i=0,j=0,dig;
    while(str[i])
    {
        strcpy(w[j++],word(str,&i));
        i+=2;
    }
    i=0;
    while(i<j)
    {
        dig=check(w[i++]);
        if(dig==10)
        {
            dig=check(w[i++]);
            num=num*10+dig;
            num=num*10+dig;
        }
        else if(dig==11)
        {
            dig=check(w[i++]);
            num=num*10+dig;
            num=num*10+dig;
            num=num*10+dig;
        }
        else
        num=num*10+dig;
    }
    printf("%ld",num);
}
```

