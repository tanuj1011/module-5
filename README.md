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
c
#include <stdio.h>

int main() {
    float length, width, area;
    float *ptrLength = &length;
    float *ptrWidth = &width;

    // Read length and width
    printf("Enter length of rectangle: ");
    scanf("%f", ptrLength);

    printf("Enter width of rectangle: ");
    scanf("%f", ptrWidth);

    // Calculate area using pointers
    area = (*ptrLength) * (*ptrWidth);

    // Display the result
    printf("Area of the rectangle: %.2f\n", area);

    return 0;
}


## OUTPUT
<img width="1635" height="638" alt="image" src="https://github.com/user-attachments/assets/d09a77f7-a889-45e0-bfff-24bd3dbfd639" />
	       	


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
c
#include <stdio.h>
#include <stdlib.h>  
#include <string.h>

int main() {
    char *str;

    str = (char *)malloc(8 * sizeof(char));  

    if(str == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }

    strcpy(str, "WELCOME");

    printf("The string is: %s\n", str);

    free(str);

    return 0;
}


## OUTPUT
<img width="1627" height="690" alt="image" src="https://github.com/user-attachments/assets/9575aeea-4229-4ebc-bec8-f718faa6165b" />



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
c
#include <stdio.h>

// Define structure for student
struct Student {
    char name[50];
    int rollNumber;
    float marks;
};

int main() {
    struct Student s;

    // Read student information
    printf("Enter student name: ");
    scanf(" %[^\n]", s.name);  // To read string with spaces

    printf("Enter roll number: ");
    scanf("%d", &s.rollNumber);

    printf("Enter marks: ");
    scanf("%f", &s.marks);

    // Display student information
    printf("\n--- Student Information ---\n");
    printf("Name       : %s\n", s.name);
    printf("Roll Number: %d\n", s.rollNumber);
    printf("Marks      : %.2f\n", s.marks);

    return 0;
}



## OUTPUT
<img width="1635" height="801" alt="image" src="https://github.com/user-attachments/assets/67373435-b0e2-4e29-a890-bc53c2d16c27" />



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
c
#include <stdio.h>
struct Employee {
    char name[50];
    int id;
    float basicSalary;
    float hra;
    float da;
    float grossSalary;
};

int main() {
    struct Employee emp[3];
    int i;
    for(i = 0; i < 3; i++) {
        printf("Enter details for Employee %d:\n", i + 1);
        printf("Name: ");
        scanf(" %[^\n]", emp[i].name);
        printf("ID: ");
        scanf("%d", &emp[i].id);
        printf("Basic Salary: ");
        scanf("%f", &emp[i].basicSalary);
        printf("HRA: ");
        scanf("%f", &emp[i].hra);
        printf("DA: ");
        scanf("%f", &emp[i].da);
        emp[i].grossSalary = emp[i].basicSalary + emp[i].hra + emp[i].da;
        printf("\n");
    }
    printf("--- Employee Details ---\n");
    for(i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("Name        : %s\n", emp[i].name);
        printf("ID          : %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basicSalary);
        printf("HRA         : %.2f\n", emp[i].hra);
        printf("DA          : %.2f\n", emp[i].da);
        printf("Gross Salary: %.2f\n", emp[i].grossSalary);
    }
    return 0;
}



 ## OUTPUT
<img width="1711" height="882" alt="image" src="https://github.com/user-attachments/assets/cc825023-ecd4-4e08-89bc-b04951097c43" />

 

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
c
#include <stdio.h>

// Define structure for student
struct Student {
    char name[10];      // Student name (optional)
    int rollno;         // Roll number (optional)
    int subject[5];     // Marks in 5 subjects
    int total;          // Total marks
    float average;      // Average marks
};

int main() {
    struct Student s[2];
    int i, j;

    // Input marks for 2 students
    for(i = 0; i < 2; i++) {
        printf("Enter marks for student %d (5 subjects):\n", i + 1);
        s[i].total = 0; // Initialize total
        for(j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
            s[i].total += s[i].subject[j]; // Add to total
        }
        s[i].average = s[i].total / 5.0; // Calculate average
    }

    // Display total and average
    for(i = 0; i < 2; i++) {
        printf("\nStudent %d Total: %d\n", i + 1, s[i].total);
        printf("Student %d Average: %.2f\n", i + 1, s[i].average);
    }

    return 0;
}



## OUTPUT
<img width="1902" height="847" alt="image" src="https://github.com/user-attachments/assets/c7431a7b-29a3-4a54-8f81-14f0228f4334" />

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
