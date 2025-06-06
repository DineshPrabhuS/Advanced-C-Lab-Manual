***EXP NO:1*** C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1. Declare structure eligible with members age (integer) and n (character array).
2. Declare variable e of type eligible.
3. Input age and name using scanf, store in e.age and e.n.
4. If e.age <= 6 print "Vaccine Eligibility: No"
5. Else print "Vaccine Eligibility: Yes"
6. Print e.age and e.n.
7. Return 0.
 
Program:

```
#include <stdio.h>
#include <string.h>
typedef struct{
    int age;
    char name[20];
    char elg[5];
}eligibility;
int main(){
    eligibility m;
    scanf("%d\n%s", &m.age, m.name);
    if(m.age > 18){
        strcpy(m.elg, "yes");
    }
    else{
        strcpy(m.elg, "no");
    }
    printf("Age:%d\n", m.age);
    printf("Name:%svaccine:%d\n", m.name, m.age);
    printf("eligibility:%s", m.elg);
}
```

Output:

![image](https://github.com/user-attachments/assets/b709672e-2432-4568-b307-884c2534232a)


Result:
Thus, the program is verified successfully. 



***EXP NO:2*** C PROGRAM TO ADD, SUBTRACT AND MULTIPLY TWO COMPLEX NUMBER USING STRUCTURE
Aim:
To write a  C Program to add, subtract and multiply two complex number using structure

Algorithm:
1. Declare structure complex with members x and y as integers.
2. Declare variables a, b, r_add, r_sub, r_mul of type complex.
3. Input values of a.x, a.y, b.x, b.y using scanf.
4. Compute r_add.x = a.x + b.x and r_add.y = a.y + b.y.
5. Compute r_sub.x = a.x - b.x and r_sub.y = a.y - b.y.
6. Compute r_mul.x = (a.x * b.x) - (a.y * b.y).
7. Compute r_mul.y = (a.x * b.y) + (b.x * a.y).
8. Print the result of addition in the format: "The no. is= r_add.x + r_add.yi"
9. Print the result of subtraction in the format: "The no. is= r_sub.x + r_sub.yi"
10. Print the result of multiplication in the format: "The no. is= r_mul.x + r_mul.yi"
11. Return 0.

Program:

```
#include <stdio.h>

struct complex{
    int x,y;
};

int main(){
    struct complex a, b, r_add,r_sub,r_mul;
    scanf("%d\n%d\n%d\n%d", &a.x, &a.y, &b.x, &b.y);
    
    r_add.x = a.x + b.x;
    r_add.y = a.y + b.y;
    
    r_sub.x = a.x - b.x;
    r_sub.y = a.y - b.y;
    
    r_mul.x = (a.x * b.x) - (a.y * b.y);
    r_mul.y = (a.x * b.y) + (b.x * a.y);
    
    printf("The no. is= %d+%di\n", r_add.x, r_add.y);
    printf("The no. is= %d+%di\n", r_sub.x, r_sub.y);
    printf("The no. is= %d+%di", r_mul.x, r_mul.y);
}
```


Output:

![image](https://github.com/user-attachments/assets/81a5caed-60df-4a06-ac01-c75fb096575b)

Result:
Thus, the program is verified successfully


 
***EXP.NO:3*** C PROGRAM TO READ A FILE NAME FROM USER AND CREATE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1. Declare a character array file to store the file name.
2. Declare a file pointer fptr.
3. Input the file name using scanf and store in file.
4. Open the file in write mode using fopen and assign to fptr.
5. Print "file File Created Successfully".
6. Print "file File Opened".
7. Close the file using fclose(fptr).
8. Print "file File Closed".
9. Return 0.
 
Program:

```
#include <stdio.h>

int main(){
    char file[20];
    FILE *fptr;
    scanf("%s", file);
    fptr = fopen(file, "w");
    printf("%s File Created Successfully\n", file);
    printf("%s File Opened\n", file);
    fclose(fptr);
    printf("%s File Closed", file);
}
```

Output:

![image](https://github.com/user-attachments/assets/4583effd-c489-4a06-b021-a576bf6f8658)


Result:
Thus, the program is verified successfully
 


***EXP NO:4*** PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:

1. Declare a character array file to store the file name.
2. Declare a file pointer fptr.
3. Input the file name using scanf and store in file.
4. Open the file in write mode using fopen and assign to fptr.
5. Print "file Opened".
6. Declare an integer variable n.
7. Input the number of lines n using scanf.
8. Declare a 2D character array line[n][20] to store n lines of text.
9. Repeat for i = 0 to n-1:
    a. Input a line of text using scanf("%[^\n]") and store in line[i].
    b. Write line[i] to file using fprintf.
10. Close the file using fclose(fptr).
11. Print "Data added Successfully".
12. Return 0.

 
Program:

```
#include <stdio.h>

int main(){
    char file[20];
    FILE *fptr;
    scanf("%s", file);
    fptr = fopen(file, "w");
    printf("%s Opened\n", file);
    int n;
    scanf("%d\n", &n);
    char line[n][20];
    for(int i = 0; i < n; i++){
        scanf("%[^\n]\n", line[i]);
        fprintf(fptr, "%s\n", line[i]);
    }
    fclose(fptr);
    printf("Data added Successfully");
}
```

Output:

![image](https://github.com/user-attachments/assets/fe8055a9-d2a7-49a0-9011-434225ad8435)


Result:
Thus, the program is verified successfully



***Ex No 5:*** TO CREATE A STRUCTURE FOR ELECTRICITY BILL CALCULATION USING TYPEDEF & FUNCTION-PASSING STRUCTURE TO A FUNCTION BY VALUE

Aim:
To create a structure for Electricity Bill calculation using typedef & function-Passing structure to a function by value (use service no, name, previous reading, current reading, unit consumption & amount as data members).

Algorithm:
1. Define structure electricityBill with members:
    - sNo (integer)
    - sName (character array)
    - prev (integer)
    - curr (integer)
    - units (integer)
    - amt (float)
2. Declare variable c of type electricityBill.
3. Input service number, service name, current reading, and previous reading using scanf, store in c.sNo, c.sName, c.curr, c.prev.
4. Calculate units consumed: c.units = c.curr - c.prev.
5. If c.units <= 100
    a. Calculate amount: c.amt = c.units * 3.
6. Else if c.units > 100 and c.units <= 300
    a. Calculate amount: c.amt = 300 + (c.units - 100) * 4.
7. Else
    a. Calculate amount: c.amt = 1100 + (c.units - 300) * 5.
8. Print service number, service name, unit consumption, and amount (formatted to 2 decimal places).
9. Return 0.


Program:

```
#include <stdio.h>
typedef struct electricityBill{
    int sNo;
    char sName[20];
    int prev, curr;
    int units;
    float amt;
}eb;
int main(){
    eb c;
    scanf("%d\n%s\n%d\n%d", &c.sNo, c.sName, &c.curr, &c.prev);
    c.units = c.curr - c.prev;
    if(c.units <= 100){
        c.amt = c.units * 3;
    }
    else if(c.units > 100 && c.units <= 300){
        c.amt = 300 + (c.units - 100) * 4;
    }
    else{
        c.amt = 1100 + (c.units - 300) * 5;
    }
    printf("service number:%d\n", c.sNo);
    printf("service name:%s\n", c.sName);
    printf("unit consumption:%d\n", c.units);
    printf("amount:%.2f", c.amt);
}
```

Output:

![image](https://github.com/user-attachments/assets/8eefdd57-e0ba-4494-9758-c97de2f22018)


Result:
Thus, the program is verified successfully
