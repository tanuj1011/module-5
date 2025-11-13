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
```
#include <stdio.h>

int main() {
    int hi,br;
    int *b=&br,*h=&hi;
    printf("Enter value of height and breadth: ");
    scanf("%d %d",h,b);
    int area=(*h)*(*b);
    printf("Area of the rectangle is: %dcm²",area);
    return 0;
    
}
```
## OUTPUT
	<img width="1036" height="302" alt="image" src="https://github.com/user-attachments/assets/93c3a068-880b-4740-97d2-3db8c97e92c3" />
	       	


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
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    char *ptr;
    ptr=(char *)malloc(sizeof("WELCOME"));
    ptr[0]='W';
    ptr[1]='E';
    ptr[2]='L';
    ptr[3]='C';
    ptr[4]='O';
    ptr[5]='M';
    ptr[6]='E';
    printf("The string is: %s",ptr);
    free(ptr);
    return 0;
    
}
```

## OUTPUT
<img width="541" height="257" alt="image" src="https://github.com/user-attachments/assets/40f19db9-2ebe-48ec-9445-9f5334c91b11" />




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
```
#include <stdio.h>
#include <stdlib.h>
typedef struct student{
    char name[100];
    int rollno;
    float marks;
}stu;
int main() {
    stu s;
    printf("Enter name, roll number and marks of a student: \n");
    scanf("%s %d %f",s.name,&s.rollno,&s.marks);
    printf("\n\nDisplaying details of the student..");
    printf("\nName of the student: %s",s.name);
    printf("\nRoll number of the student: %d",s.rollno);
    printf("\nMarks scored by the student: %.2f",s.marks);
    return 0;
    
}
```

## OUTPUT
<img width="1032" height="402" alt="image" src="https://github.com/user-attachments/assets/fa8f7214-4757-4576-b93a-6ed125143c3b" />


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
```
#include <stdio.h>
#include <stdlib.h>
typedef struct employees{
    char name[100];
    int id;
    float bpay;
    float hra;
    float da;
    float gross;
}emp;
int main() {
    emp e;
    printf("Enter name, id and basic pay of a employee: \n");
    scanf("%s %d %f",e.name,&e.id,&e.bpay);
    e.hra=(float)e.bpay*30/100;
    e.da=(float)e.bpay*10/100;
    e.gross=e.bpay+e.hra+e.da;
    printf("\n\nDisplaying details of the student..");
    printf("\nName of the employee: %s",e.name);
    printf("\nID of the employee: %d",e.id);
    printf("\nBasic Pay of the employee: %.2f",e.bpay);
    printf("\nGross Salary of the employee: %.2f",e.gross);
    return 0;
    
}
```

 ## OUTPUT

<img width="692" height="548" alt="image" src="https://github.com/user-attachments/assets/2c91a2c7-1562-4889-a058-de62448132af" />
 

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
```
#include <stdio.h>
#include <stdlib.h>
typedef struct student{
    char name[100];
    int rollno;
    int sub[5];
    int total;
}stu;
int main() {
    stu s[2];
    for(int i=0;i<2;i++){
        printf("Enter Student Details(name,rollno): ");
        scanf("%s %d",s[i].name,&s[i].rollno);
        printf("Enter mark scored in five subjects: ");
        s[i].total=0;
        for(int j=0;j<5;j++){
            scanf("%d",&s[i].sub[j]);
            s[i].total+=s[i].sub[j];
        }
        
    }
    printf("\nDisplaying totals of the students stored:\n");
    for(int i=0;i<2;i++){
        printf("Total of student %d is: %d\n",i+1,s[i].total);
    }
    return 0;
    
}
```

## OUTPUT
<img width="775" height="517" alt="image" src="https://github.com/user-attachments/assets/e397941f-5d92-4ee2-9598-716d3301e732" />

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


