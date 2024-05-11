# Ex-3 GENERATION OF LEXICAL TOKENS USING C
# AIM
## To write a C program to implement lexical analyzer to recognize a few patterns.
# ALGORITHM
1)	Start the program.
2)	Get the input from the user with the terminating symbol ‘;’.
3)	Until the symbol is ‘;’, do the following:
   
    a.	If the next character of the symbol is an operator then print it as an operator.
  	
    b.	If the next character of the symbol is a variable, then insert it into symbol table and print it as an identifier.
  	
    c.	If the next character of the symbol is a bracket, then print it as parenthesis.
  	
5)	Stop the program.
# PROGRAM
```
#include<stdio.h>
#include<conio.h> 
#include<ctype.h> 
#include<malloc.h> 
#include<string.h> 
#include<math.h>
void main()
{
int i=0,j=0,x=0,n,flag=0; void *p,*add[5];
char ch,srch,b[15],d[15],c; 
printf("Enter the Expression terminated by $: ");
while((c=getchar())!='$')
{
b[i]=c; i++;
}
n=i-1;
printf("Given Expression:"); i=0;
while(i<=n)
{
printf("%c",b[i]); i++;
}
printf("\n Symbol Table\n"); printf("Symbol\taddr\ttype"); while(j<=n)
{
c=b[j]; if(isalpha(toascii(c)))
{
if(j==n)
{
p=malloc(c); add[x]=p;
d[x]=c;
printf("%c\t%d\tidentifier",c,p);
}
else
{
ch=b[j+1];
if(ch=='+'||ch=='-'||ch=='*'||ch=="=")
{
p=malloc(c); add[x]=p;
d[x]=c; printf("\n%c\t%d\tidentifier\n",c,p); x++;
}}} j++;
}
printf("\n The symbol is to be searched"); srch=getch();
for(i=0;i<=x;i++)
{
if(srch==d[i])
{
printf("\n Symbol Found"); printf("\n%c%s%d\n",srch,"@address",add[i]); flag=1;
}
}
if(flag==0)
printf("\nSymbol Not Found"); 
getch();
}
```
# OUTPUT
![Screenshot 2024-04-08 114401](https://github.com/23014107/Ex-3-GENERATION-OF-LEXICAL-TOKENS-/assets/151625620/a5df0278-9d2c-4c6a-bcf7-33a48463064a)

# RESULT
### The program to implement lexical analyzer is executed and the output is verified.
