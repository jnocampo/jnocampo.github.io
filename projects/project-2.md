---
layout: project
type: project
image: images/bank.png
title: bankDatabase
permalink: projects/bankDatabase
# All dates must be YYYY-MM-DD format!
date: 2019-04-30
labels:
  - C
  - C++
  - GitHub
summary: database functions for the bank database application.
---

<img class="ui medium right floated rounded image" src="../images/bank.png">

This program holds a database of user accounts and displays a menu of different choices for the user to interact with the accounts inside the database. It also allows user to create new accounts. Each account holds the users information such as name, birthdate, account number, etc.  


For my class, I wrote this in C and in C++.



getAddress in C:


```js
void getaddress (char *address, int lineChars)
{
    char str[100];

    if (debug == 1)
    {
        printf("----- getAddress DEBUG ----- \n");
        printf("----- lineChars : %d\n", lineChars);
    }   
     
    printf("Enter the address of the account : \n");
    printf("Include '^' at the end to indicate the end of the address : \n ");

    strcpy(address, "");
    while (fgets(str, 99, stdin))
    {
        fseek(stdin, 0, SEEK_END);
        if (str[strlen(str) - 2] == '^') {
            strcat(address, str);
            fseek(stdin, 0, SEEK_END);
            break;
        }
        else
        {
            strcat(address, str);
        }
    }
    strcpy(str, "");
}
```



getAddress in C++:



```js

void getaddress(char address[])
{
    char user_input[100];
    
    #if DEBUG == 1
        cout << "----- DEBUG getAddress -----" << endl;
        cout << "Address : " << address << endl;
    #endif
 
    cout << "Enter the address of the account : " << endl;
    cout << "Include '^' at the end to indicate the end of the address : " << endl;

    cin.ignore();

    while(cin.getline(user_input, 99))
    {
        if(user_input[strlen(user_input) - 1] == '^') {
            strcat(address, user_input);
            fseek(stdin, 0, SEEK_END);
            break;
        }
        else
        {
            strcat(address, user_input);
            strcat(address, "\n");
        }
    }
    strcpy(user_input, "");
}
```



[Project Informaiton]() 

[My Work in C](https://github.com/jnocampo/ICS-212) 

[My Work in C++](https://github.com/jnocampo/ics212-project2)
 
