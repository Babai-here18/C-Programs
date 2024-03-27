# Conditional or Ternary Operator

### 1. WAP. to input a number and print even or odd.

> Test Data

    Enter a number: 5

> Expected Output

    5 is a Odd number.

> Source Code

```c
#include <stdio.h>

int main(){
    int num;

    printf("Enter a number:");
    scanf("%d", &num);

    num % 2 == 0 ? printf("Even Number.") : printf("Odd number");

    return 0;
}
```

<br>

### 2. WAP. to find the greatest of the two numbers.

> Test Data

    Enter two number: 5 10

> Expected Output

    Greater number = 10

> Source Code

```c
#include <stdio.h>

int main(){
    int num1, num2, great;

    printf("Enter two number: ");
    scanf("%d %d", &num1, &num2);

    great = num1 > num2 ? num1 : num2;

    printf("Greater number = %d", great);

    return 0;
}
```

<br>

### 3. WAP. to find the greatest of the three numbers.

> Test Data

    Enter Three number: 22 43 10

> Expected Output

    Greater number = 43

> Source Code

```c
#include <stdio.h>

int main(){
    int num1, num2, num3, great;

    printf("\nEnter three number: ");
    scanf("%d %d %d", &num1, &num2, &num3);

    great = num1 > num2 ? num1 > num3 ?
    num1 : num3 : num2 > num3 ? num2 : num3;

    printf("\nGreater number = %d", great);

    return 0;
}
```

<br>

### 4. WAP. using conditional operators to determine whether a year entered through the keyboard is a leap year or not

> Test Data

    Enter a year: 2021

> Expected Output

    Not a leap year.

> Source Code

```c
#include <stdio.h>

int main(){
    int year;

    printf("\nEnter a year:");
    scanf("%d", &year);

    year % 4 == 0 ? printf("\nLeap year.") :
    year % 100 != 0 && year % 400 == 0 ?
    printf("\nLeap year.") : printf("\nNot a Leap year.");

    return 0;
}
```

<br>

### 5. WAP. The cost of one type of mobile service is Rs. 250 plus Rs. 1.25 for each call made over and above 100 calls. print the bill. (ternary operator)

> Test Data

    Enter number of Calls: 200

> Expected Output

    Total Bill = 251.25

> Source Code

```c
#include <stdio.h>

int main(){
    float calls, bill;

    printf("Enter number of Calls: ");
    scanf("%f", &calls);

    bill = calls > 100 ?(250 + (calls - 100) * 1.25 ): 250;

    printf("Total Bill = %.2f", bill);

    return 0;
}
```

<br>

### 6. WAP. to find Whether the character entered through the keyboard is a lower case alphabet or uppercase.

> Test Data

    Enter a character: a

> Expected Output

    Character is Lowercase.

> Source Code

```c
#include <stdio.h>

int main(){
    char ch;

    printf("Enter a character: ");
    scanf("%c", &ch);

    ch >= 65 && ch <= 90 ? printf("Character is Uppercase.") :
    ch >= 97 && ch <= 121 ? printf("Character is Lowercase.") :
    printf("Not a character.");

    return 0;
}
```
<br>

<h1 align="center">Hi 👋, I'm Babai</h1>
<h3 align="center">A passionate frontend developer from India</h3>
 
<br>   
