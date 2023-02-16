# Basic-string-operations-in-C
Different basic string operations in C programming



date : 13;04;2021(ugadi)
basic string operations
1..)
#include<stdio.h>
#include<string.h>
void main()
{
    char k1[10],k2[10],k3[10],k4[10],k5[10],k;
    int a,b,c;
    printf("Enter string1 and string2\n");
    scanf("%s%s",k1,k2);
    printf("length of %s is %d ",k1,strlen(k1));
    printf("The copied string of %s and %s is\n",k1,strcpy(k3,k1));
    b = strcmp(k1,k2);
    if(b==0)
    printf("both strings are equal \n");
    else if(b>0)
    printf("%s is greather than %s",k1,k2);
    printf("cancatetanation of both strings %s and %s is %s\n",k1,k2,strcat(k1,k2));
}

o/p:
Enter string1 and string2
pandu
kalyan
length of pandu is 5 The copied string of pandu and pandu is
pandu is greather than kalyancancatetanation of both strings pandukalyan and kalyan is pandukalyan


2....)
check given word is polindrome or not
#include<stdio.h>
void main()
{
    char str[30],k1[30];
    int i,j,len,flag;
    printf("Enter a string : ");
    gets(str);//AMMA 
    len = strlen(str);// 4
    i=0;
    j=len-1;//4-1 = 3
    flag = 0;//flag used to know change is there or not
    while(i<j)//(0 < 3) 0,1,2 three times true forth time false( 3 < 3)
    {
        if(str[i] == str[j])//comparing 1st letter and last letter of the word
        {
            i++;//if true check all the other letters
            j--;
        }
        else
        {
            flag = 1;//flage changed because str[0] != str[1](not polindrome)
            break;
        }
    }
    if(flag == 0)
        printf("Given word %s is polindrome",str);
    else
        printf("Given word %s is not is polindrome",str);
}

o/p:
	Enter a string : NANNA
Given word NANNA is not is polindrome

3.....)

#include<stdio.h>
int kalyan(int x, int y); //decleration of function
void main()
{
    int a,b,c;
    printf("Enter a and b values : ");
    scanf("%d %d",&a,&b);
    c = kalyan(a,b); //calling the function
    printf("a*b = %d",c);
}
int kalyan(int x, int y)//defineing the function
{
    int z;
    z = x * y;//called function doing process
    return z;
}
o/p:
Enter a and b values : 1
3
a*b = 3







\\the End
