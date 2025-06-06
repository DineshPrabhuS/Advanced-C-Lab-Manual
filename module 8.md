EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER

Aim:
To write a C program print the lowercase English word corresponding to the number

Algorithm:
1. Define recursive function myPow(n, x):
    a. If x == 0, return 1
    b. Else return n * myPow(n, x-1)
2. In main function:
3. Declare integer n
4. Input integer n using scanf
5. If 1 <= n <= myPow(10, 9):
    a. Switch on n:
        - case 41: print "forty one"
        - case 42: print "forty two"
        - case 43: print "forty three"
        - case 44: print "forty four"
        - case 45: print "forty five"
        - case 46: print "forty six"
        - case 47: print "forty seven"
        - case 48: print "forty eight"
        - case 49: print "forty nine"
    b. If n > 49:
        - print "Greater than 49"
6. End

 
Program:

```
#include <stdio.h>
int myPow(int n, int x){
    if(x == 0){
        return 1;
    }
    return n * myPow(n, x-1);
}
int main(){
    int n;
    scanf("%d", &n);
    if(1 <= n && n <= myPow(10, 9)){
        switch(n){
            case 41:
            printf("forty one\n");
            break;
            case 42:
            printf("forty two\n");
            break;
            case 43:
            printf("forty three\n");
            break;
            case 44:
            printf("forty four\n");
            break;
            case 45:
            printf("forty five\n");
            break;
            case 46:
            printf("forty six\n");
            break;
            case 47:
            printf("forty seven\n");
            break;
            case 48:
            printf("forty eight\n");
            break;
            case 49:
            printf("forty nine\n");
            break;
        }
        if(n > 49){
        printf("Greater than 49\n");
    }
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/4d9986d6-9770-4c87-94f0-2b3c0470b51e)


Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .

Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.

Algorithm:
1. Declare a character array s of size 20.
2. Declare an integer array count of size 10, initialized to 0.
3. Declare an integer n.
4. Input a string with spaces using scanf("%[^\n]%*c") and store in s.
5. For each character s[i] in the string until null character:
    a. If s[i] is a digit between '0' and '9':
        i. Convert character to integer: n = s[i] - '0'.
        ii. Increment count[n] by 1.
6. For i from 0 to 9:
    a. Print count[i] followed by a space.
7. End.

 
Program:

```
#include <stdio.h>

int main(){
    char s[20];
    int count[10] = {0};
    int n;
    scanf("%[^\n]%*c", s);
    for(int i = 0; s[i] != '\0'; i++){
        if('0' <= s[i] && s[i] <= '9'){
            n = s[i] - '0';
            count[n] += 1;
        }
    }
    for(int i = 0; i < 10; i++){
        printf("%d ", count[i]);
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/beca5096-bf98-460e-affa-f05e740def81)


Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.

Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1. Define function permutation with parameters: integer n and array of string pointers s.
2. Initialize i = n - 2.
3. While i >= 0 and s[i] >= s[i+1] (lexicographically):
    a. Decrement i by 1.
4. If i < 0, return 0 (no more permutations).
5. Initialize j = n - 1.
6. While s[j] <= s[i]:
    a. Decrement j by 1.
7. Swap s[i] and s[j].
8. Reverse the sub-array s[i+1] to s[n-1].
9. Return 1.
10. In main function:
11. Input integer n.
12. Allocate memory for array s of n string pointers.
13. For i from 0 to n-1:
    a. Allocate memory for s[i] (11 chars).
    b. Input string into s[i].
14. Do:
    a. Print all strings s[i] separated by spaces.
15. While permutation(n, s) returns 1.
16. Free all allocated memory for strings and array s.
17. Return 0.

 
Program:

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int permutation(int n,char **s){
        int i=n-2;
        
        while(i>=0 && strcmp(s[i], s[i+1])>=0)
            i--;
        if(i<0) return 0;
        
        int j=n-1;
        while(strcmp(s[j],s[i]) <= 0)
            j--;
            
        char *temp=s[i];
        s[i]=s[j];
        s[j]=temp;
        
        for(int j=i+1,k=n-1;j<k;j++,k--){
            temp=s[j];
            s[j]=s[k];
            s[k]=temp;
        }
        return 1;
}

int main(){
     
     int n;
     scanf("%d",&n);
     
     char **s=malloc(n*sizeof(char *));
     
     for(int i=0;i<n;i++){
         s[i]=malloc(11*sizeof(char));
         scanf("%s",s[i]);
     }
     do{
        for(int i=0;i<n;i++){
            printf("%s%c",s[i],i==n-1 ? '\n':' ');
        } 
     }while(permutation(n,s));
     
     for(int i=0;i<n;i++){
         free(s[i]);
     }
     free(s);
    return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/d143565f-6ec0-4aaf-b5e9-152e2df54616)



Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.

![image](https://github.com/user-attachments/assets/a5b07da2-09e5-4530-939a-28cc74b8c799)

Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.

Algorithm:
1. Input integer n.
2. Calculate k = 2 * n - 1.
3. For i from 0 to k-1:
    a. For j from 0 to k-1:
        i. val = minimum of (i, j, k-1-i, k-1-j)
        ii. Print (n - val) followed by a space.
    b. Print newline.
4. Return 0.

 
Program:

```
#include <stdio.h>

int main() 
{
    int n;
    scanf("%d", &n);
    int k = 2 * n - 1;
    int val;
  	for(int i = 0; i < k; i++){
        for(int j = 0; j < k; j++){
            val = i < j ? i : j;
            val = val < (k - i - 1) ? val : (k - i - 1);
            val = val < (k - j - 1) ? val : (k - j - 1);
            printf("%d ", n - val);
        }
        printf("\n");
    }
    
    return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/a462b1d4-7cd5-4b30-ae56-704382327935)


Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.

Aim:

To write a C program that prints sum of the integers in the array.

Algorithm:

1. Declare integer variables n and sum, initialize sum to 0.
2. Input integer n.
3. Declare integer pointer arr.
4. Dynamically allocate memory for n integers and assign to arr.
5. For i from 0 to n-1:
    a. Input integer value into arr[i].
    b. Add arr[i] to sum.
6. Print sum.
7. Free the dynamically allocated memory arr.
8. Return 0.


Program:

```
#include <stdio.h>
#include <stdlib.h>

int main(){
    int n, sum = 0;
    scanf("%d", &n);
    int *arr;
    arr= (int *) malloc (n * sizeof(int *));
    for(int i = 0; i < n; i++){
        scanf("%d ", &arr[i]);
        sum += arr[i];
    }
    printf("%d", sum);
    free(arr);
}
```

Output:

![image](https://github.com/user-attachments/assets/c0545e59-59ac-4002-a6fc-9d2afbc9b157)

![image](https://github.com/user-attachments/assets/b3c9df00-689b-44c7-a213-b6bca7b27e90)


Result:
Thus, the program is verified successfully

