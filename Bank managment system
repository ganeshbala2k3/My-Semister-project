//bank management system

#include<stdio.h>
#include<stdlib.h>
#include<math.h>
#include<string.h>
struct Account{    //declaration of structure
    long int accountnumber;
    char name[100];
    int balance;
}bank[1000];
int count=0;
void Password();
void create();
void display();
void knowbalance();
void withdraw();
int main()
{
    //login credentials
    printf("welcome to bank management system\n\n\nplease enter the login credentials \n\n");
    char email[100]="email.com";
    char x[1000];
    printf("enter the email address\n");
    scanf("%s",x);
    if(strcmp(x,email)!=0)
    {
        printf("please try again!");
        main();
    }
    printf("enter the password\n");
    Password();
    int n;
    while(1)
    {
    printf("1.create new bank account\n\n2.display all bank accounts\n\n3.withdraw money\n\n4.know your balance\n\n");
 printf("enter your choice\n");
 scanf("%d",&n);
 switch(n)
 {
     case 1:  create();
     break;
     case 2:  display();
     break;
     case 3:  withdraw();
     break;
     case 4:  knowbalance();
     break;
     default: printf("wrong choice\n");
 }
    }
 return 0;   
    
}
void Password()       //Passoword which need be encyrpted
{
     char p[100]="password";
     char y[1000];
     scanf("%s",y);
     if(strcmp(y,p)!=0)
     {
         printf("please retry the password again!\n");
         Password();
     }
}
void create()     //create bank account 
{
    int n;
    printf("No of accounts to get created\n");
    scanf("%d",&n);
    for(int i=0;i<n;i++)
    {
        printf("enter the new account number to be made\n");
        scanf("%ld",&bank[i].accountnumber);
        printf("enter the name\n");
        scanf("%s",bank[i].name);
        printf("enter the ammount to be added\n");
        scanf("%d",&bank[i].balance);
    }
    for(int i=0;i<n;i++)
    {
        printf("\n****************************\n");
        printf("\nAccount number : %ld\nname of benificiery:%s \n Account balance : %d\n Account created successfully!\n",bank[i].accountnumber,bank[i].name,bank[i].balance);
    printf("\n****************************\n");
        
    }
   count=count+n;
}
void display()        //display all bank accounts
{
    for(int i=0;i<count;i++)
    {
        printf("\n\n*************\nAccount number: %ld\nname:%s\naccount balance:%d\n*************\n\n",bank[i].accountnumber,bank[i].name,bank[i].balance);
    }
}
void knowbalance()   //know your balance
{
    long int k,flag=0;
    printf("enter the account number\n");
    scanf("%ld",&k);
    for(int i=0;i<count;i++)
{
    if(k==bank[i].accountnumber)
    {
        flag=1;
        printf("\n*************\nbalance of the account %s\n account number:%ld\n balance :%d\n*************\n",bank[i].name,bank[i].accountnumber,bank[i].balance);
        break;
    }
    if(flag==0)
    {
    printf("Account is not found\n");
    }
}
}
void withdraw()        //withdraw the ammount
{
 long int k;
 int flag=0;
 int x;
    printf("enter the account number\n");
    scanf("%ld",&k);
    printf("enter the ammount to get withdrawn\n");
    scanf("%d",&x);
    for(int i=0;i<count;i++)
{
    if(bank[i].accountnumber==k)
    {
        flag=1;
        printf("\n\n*************\nCURRENT BALANCE OF %s\n account number:%ld\n balance :%d\n*************\n",bank[i].name,bank[i].accountnumber,(bank[i].balance-x));
        bank[i].balance=bank[i].balance-x;
        break;
    }
    if(flag==0)
    {
    printf("Account is not found\n");
    }
}
}



