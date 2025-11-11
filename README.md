## Name: Naneshvaran C
## REg.no:212224110038
EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:
```
#include <stdio.h>

int main() {
    int n;

    printf("Enter a number: ");
    scanf("%d", &n);

    switch(n) {
        case 71: 
            printf("seventy one\n"); 
            break;
        case 72: 
            printf("seventy two\n"); 
            break;
        case 73: 
            printf("seventy three\n"); 
            break;
        case 74: 
            printf("seventy four\n"); 
            break;
        case 75: 
            printf("seventy five\n"); 
            break;
        case 76: 
            printf("seventy six\n"); 
            break;
        case 77: 
            printf("seventy seven\n"); 
            break;
        case 78: 
            printf("seventy eight\n"); 
            break;
        case 79: 
            printf("seventy nine\n"); 
            break;
        default: 
            printf("Greater than  80\n");
    }

    return 0;
}
```

Output:

<img width="1432" height="717" alt="image" src="https://github.com/user-attachments/assets/c3c3fe93-7db9-4692-9a37-753703123674" />

Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include <stdio.h>
#include <string.h>

int main() {
    char a[50];
    int i, j, c;
    
    printf("Enter a string of digits: ");
    scanf("%s", a);

    for(j = 0; j <= 3; j++) {
        c = 0;
        for(i = 0; i < strlen(a); i++) {
            if(a[i] - '0' == j) {
                c++;
            }
        }
        printf("%d ", c);
    }

    printf("\n");
    return 0;
}
```
Output:

<img width="1377" height="629" alt="image" src="https://github.com/user-attachments/assets/4a1242c4-7cd2-417a-9dc7-7887b88874b6" />

Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

// Function to compare characters for qsort
int cmp(const void *a, const void *b) {
    return (*(char *)a - *(char *)b);
}

// Function to swap two characters
void swap(char *x, char *y) {
    char temp = *x;
    *x = *y;
    *y = temp;
}

// Function to reverse a substring from start to end indices
void reverse(char *str, int start, int end) {
    while(start < end) {
        swap(&str[start], &str[end]);
        start++;
        end--;
    }
}

// Function to generate the next lexicographical permutation
int nextPermutation(char *str) {
    int n = strlen(str);
    int i = n - 2;

    // Step 1: Find the rightmost character which is smaller than its next character
    while(i >= 0 && str[i] >= str[i + 1])
        i--;

    if(i < 0)
        return 0; // Last permutation reached

    // Step 2: Find the smallest character on right of i, which is greater than str[i]
    int j = n - 1;
    while(str[j] <= str[i])
        j--;

    // Step 3: Swap characters at i and j
    swap(&str[i], &str[j]);

    // Step 4: Reverse the substring after position i
    reverse(str, i + 1, n - 1);

    return 1;
}

int main() {
    char str[50];

    printf("Enter a string: ");
    scanf("%s", str);

    // Sort the string initially to get the first permutation
    qsort(str, strlen(str), sizeof(char), cmp);

    printf("Permutations in lexicographical order:\n");
    do {
        printf("%s\n", str);
    } while(nextPermutation(str));

    return 0;
}
```
Output:
<img width="1452" height="661" alt="image" src="https://github.com/user-attachments/assets/556565ed-d8d5-45dd-8d5e-1a17fe9c7711" />

Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
```
#include <stdio.h>

int main() {
    int n, len, i, j, min;

    printf("Enter n: ");
    scanf("%d", &n);

    len = 2 * n - 1;

    for(i = 0; i < len; i++) {
        for(j = 0; j < len; j++) {
            min = i < j ? i : j;
            min = min < (len - 1 - i) ? min : (len - 1 - i);
            min = min < (len - 1 - j) ? min : (len - 1 - j);
            printf("%d ", n - min);
        }
        printf("\n");
    }

    return 0;
}
```

Output:
<img width="1304" height="652" alt="image" src="https://github.com/user-attachments/assets/7d522f29-c76e-42a9-acaf-39b7941eb83c" />


Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:
```
#include <stdio.h>

int square() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num * num;
}

int main() {
    int result;
    result = square();
    printf("Square of the number is: %d\n", result);
    return 0;
}
```

Output:

<img width="1444" height="515" alt="image" src="https://github.com/user-attachments/assets/1c297512-5742-4924-aae5-38e1ed9f8d95" />

Result:
Thus, the program is verified successfully



























