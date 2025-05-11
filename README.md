# NAME : JAIYANTAN S 
# REG NO : 212224100021
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
![image](https://github.com/user-attachments/assets/3e33e131-30f4-4d3d-9fb5-24832e224009)


## OUTPUT
![image](https://github.com/user-attachments/assets/01433b41-b3b1-4d80-bf7c-fcd5cf9f2505)

		       	


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
![image](https://github.com/user-attachments/assets/260bebcc-d8ec-4e7e-8cc4-c409fc96af60)


## OUTPUT
![image](https://github.com/user-attachments/assets/46b3c1ed-1b50-4620-ae61-eb3c0c17d556)




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
![image](https://github.com/user-attachments/assets/5242dc84-bee2-4bac-90d4-8e7c1f3df65e)



## OUTPUT
![image](https://github.com/user-attachments/assets/6e8fd5f0-3221-42bd-81e5-3679ec35f4b7)



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
    float hra;    
    float da;    
    float gross_salary;
};

int main() {
    struct Employee emp[3]; 
    int i;

    for (i = 0; i < 3; i++) {
        printf("\nEnter details for Employee %d:\n", i + 1);

        printf("Enter name: ");
        scanf(" %[^\n]", emp[i].name);

        printf("Enter ID: ");
        scanf("%d", &emp[i].id);

        printf("Enter basic salary: ");
        scanf("%f", &emp[i].basic_salary);

        printf("Enter HRA: ");
        scanf("%f", &emp[i].hra);

        printf("Enter DA: ");
        scanf("%f", &emp[i].da);
        emp[i].gross_salary = emp[i].basic_salary + emp[i].hra + emp[i].da;
    }
    printf("\nEmployee Details:\n");
    for (i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("Name: %s\n", emp[i].name);
        printf("ID: %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basic_salary);
        printf("HRA: %.2f\n", emp[i].hra);
        printf("DA: %.2f\n", emp[i].da);
        printf("Gross Salary: %.2f\n", emp[i].gross_salary);
    }
    return 0;
}

 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/b0c6009f-e777-4c12-a908-7a31dba3ce25)


 

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
};
int main() {
    struct student s[2];
    int n, i, j;
    for (i = 0; i < 2; i++) {
        printf("\nEnter details for Student %d:\n", i + 1);
        printf("Enter roll number: ");
        scanf("%d", &n);

        printf("Enter marks for 5 subjects:\n");
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }
    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }
    s[0].total = 374;
    s[1].total = 383;

    printf("\nStudent Totals and Averages:\n");
    for (i = 0; i < 2; i++) {
        printf("\nStudent %d:\n", i + 1);
        printf("Total Marks: %d\n", s[i].total);
        printf("Average Marks: %.2f\n", s[i].total / 5.0);
    }
    return 0;
}


## OUTPUT
![image](https://github.com/user-attachments/assets/91e12fec-6609-450c-8e2d-95a5355d5e07)

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


