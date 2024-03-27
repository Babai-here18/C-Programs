# Structure

### 1. Write a program to store and print the roll no., name , age and marks of a student using structures. 

> Test Data

    Enter 'Roll Number', 'Name' and 'Marks' of 5 students: 
    Student 1: 1 Parth 90
    Student 2: 2 Mehak 94
    Student 3: 3 Arpit 95
    Student 4: 4 Karthik 96
    Student 5: 5 Bhavya 80

> Expected Output
    
    Student details:
        Roll Number         Name          Marks
        1                   Parth         90
        2                   Mehak         94
        3                   Arpit         95
        4                   Karthik       96
        5                   Bhavya        80
        
> Source Code

```c
#include <stdio.h>

struct student {
    int rollNo;
    char name[30];
    int marks;
};

void inputData(struct student students[], int length){
    printf("\nEnter 'Roll Number', 'Name' and 'Marks' of 5 students: ");
    for(int i = 0; i < length; i++){
        printf("\nStudent %d: ", i+1);
        scanf("%d%s%d", &students[i].rollNo, &students[i].name,
         &students[i].marks);
    }
}
void printData(struct student students[], int length){
    printf("\n\tStudent details: ");
    printf("\n\t\tRoll Number\t\tName\t\tMarks");
    for(int i = 0; i < length; i++){
        printf("\n\t\t%d\t\t\t%s\t\t%d", students[i].rollNo,
         students[i].name, students[i].marks);
    }
}
int main(){
    struct student students[5];
    int length = 5;
    
    inputData(students, length);
    printData(students, length);
    return 0;
}
```

<br>

### 2. Enter the marks of 5 students in Chemistry, Mathematics and Physics (each out of 100) using a structure named Marks having elements roll no., name, chem_marks, maths_marks and phy_marks and then display the percentage of each student. 

> Test Data

    Enter Roll Number, Name, Chemistry, Math, Physics of 5 Students:

    Student 1: 1 Parth 90 92 89
    Student 2: 2 Mehak 92 94 86
    Student 3: 3 Arpit 96 94 92
    Student 4: 4 Karthik 92 95 90
    Student 5: 5 Bhavya 90 89 92

> Expected Output

    Roll Number     Name      Chemistry    Math     Physics     Total    Percentage
    
    1               Parth     90           92       89          271      90.33%
    2               Mehak     92           94       86          272      90.67%
    3               Arpit     96           94       92          282      94.00%
    4               Karthik   92           95       90          277      92.33%
    5               Bhavya    90           89       92          271      90.33%

> Source Code

```c
#include <stdio.h>

struct student{
    int roll;
    char name[30];
    int chem_marks, maths_marks, phy_marks;
};
void inputData(struct student students[], int length){
    int i;
    printf("\nEnter Roll Number, Name, Chemistry, Math, Physics of 5 Students:\n");
    for(i = 0; i < length; i++){
        printf("\nStudent %d: ", i+1);
        scanf("%d%s%d%d%d", &students[i].roll, &students[i].name,
        &students[i].chem_marks, &students[i].maths_marks,
        &students[i].phy_marks);
    }
}
void printData(struct student students[], int length){
    int i, total;
    float per;
    printf("\n\tRoll Number\tName\t\tChemistry\tMath\t\tPhysics\t\tTotal\t\tPercentage\n");
    for(i = 0; i < length; i++){
        total = students[i].chem_marks + students[i].maths_marks + students[i].phy_marks;
        per = total / 300.0 * 100;
        printf("\n\t%d\t\t%s\t\t%d\t\t%d\t\t%d\t\t%d\t\t%.2f%%\n", students[i].roll, students[i].name,
        students[i].chem_marks, students[i].maths_marks,
        students[i].phy_marks, total, per);
    }
}
int main(){
    struct student students[5];
    int length = 5;

    inputData(students, length);
    printData(students, length);
    return 0;
}
```
<br>

<h1 align="center">Hi 👋, I'm Babai</h1>
<h3 align="center">A passionate frontend developer from India</h3>
 
<br>   

