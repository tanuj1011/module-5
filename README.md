# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM


#include<stdio.h>
int main(){
    int l,b;
    int *pl=&l;
    int *pb=&b;
    printf("Enter the length and breadth of the rectangle: ");
    scanf("%d %d",pl,pb);
    int area=(*pl)*(*pb);
    printf("Area of the rectangle : %d",area);
    return 0;
}

## OUTPUT
		       	
<img width="1674" height="764" alt="Screenshot 2025-10-20 160233" src="https://github.com/user-attachments/assets/5f2cab77-2f0d-48e2-a820-7af1ee3cf711" />


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM

#include <stdio.h>
#include <stdlib.h> 
#include <string.h>

int main() {
    char *str;
    str = (char *)malloc(8 * sizeof(char));

    if (str == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }
    strcpy(str, "WELCOME");
    printf("%s\n", str);
    free(str);
    return 0;
}

## OUTPUT

<img width="1563" height="751" alt="Screenshot 2025-10-20 160834" src="https://github.com/user-attachments/assets/d2a20107-e2be-473c-a311-2dc94411e755" />


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM

#include<stdio.h>
struct stu{
  char name[50];
  int id;
  int mark;
};
int main(){
    struct stu s;
    scanf("%s %d %d",s.name,&s.id,&s.mark);
    printf("Student details:\n");
    printf("Name:%s\nRoll No.:%d\nMarks:%d",s.name,s.id,s.mark);
    return 0;
}



## OUTPUT

 <img width="1919" height="768" alt="Screenshot 2025-10-20 161734" src="https://github.com/user-attachments/assets/760dc238-e6f5-47ad-a4f1-54066f5eb716" />
 
## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM

#include <stdio.h>
struct Employee {
    char name[50];
    int id;
    float basic_salary;
    float gross_salary;
};
int main() {
    struct Employee emp[3];
    int i;
    for(i = 0; i < 3; i++) {
        printf("\nEnter details of Employee %d:\n", i + 1);
        printf("Enter Name: ");
        scanf("%s", emp[i].name);
        printf("Enter ID: ");
        scanf("%d", &emp[i].id);
        printf("Enter Basic Salary: ");
        scanf("%f", &emp[i].basic_salary);
        float hra = emp[i].basic_salary * 0.20;
        float da  = emp[i].basic_salary * 0.10;
        emp[i].gross_salary = emp[i].basic_salary + hra + da;
    }

    printf("\n--- Employee Details with Gross Salary ---\n");
    for(i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("Name: %s\n", emp[i].name);
        printf("ID: %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basic_salary);
        printf("Gross Salary: %.2f\n", emp[i].gross_salary);
    }
    return 0;
}

 ## OUTPUT


<img width="1776" height="807" alt="Screenshot 2025-10-20 162414" src="https://github.com/user-attachments/assets/2c6c8409-0e03-468a-a0cb-e6e397b26b5d" />


## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM

#include <stdio.h>
struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
    float average;
};
int main() {
    struct student s[2];
    int i, j;
    for (i = 0; i < 2; i++) {
        printf("\nEnter details of Student %d:\n", i + 1);
        printf("Enter Name: ");
        scanf("%s", s[i].name);
        printf("Enter Roll Number: ");
        scanf("%d", &s[i].rollno);
        printf("Enter marks of 5 subjects:\n");
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }
    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0;
    }
    printf("\n--- Student Total and Average Marks ---\n");
    for (i = 0; i < 2; i++) {
        printf("\nStudent %d\n", i + 1);
        printf("Name: %s\n", s[i].name);
        printf("Roll Number: %d\n", s[i].rollno);
        printf("Total Marks: %d\n", s[i].total);
        printf("Average Marks: %.2f\n", s[i].average);
    }
    return 0;
}


## OUTPUT

 <img width="1804" height="786" alt="Screenshot 2025-10-20 163222" src="https://github.com/user-attachments/assets/a21c8f58-8793-4d56-a957-896a38d688e8" />


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
