## Name: Naneshvaran C
## Reg.no:212224110038

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include <stdio.h>

// Function to find the greatest of three numbers
int findGreatest(int a, int b, int c) {
    int max = a;
    if(b > max)
        max = b;
    if(c > max)
        max = c;
    return max;
}

int main() {
    int num1, num2, num3;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &num1, &num2, &num3);

    int greatest = findGreatest(num1, num2, num3);

    printf("The greatest number is: %d\n", greatest);

    return 0;
}
```
Output:
<img width="1419" height="697" alt="image" src="https://github.com/user-attachments/assets/2460e7df-f29d-4a0a-8fb9-38cccd40bb33" />


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include <stdio.h>

int main() {
    int n;
    int maxAnd = 0, maxOr = 0, maxXor = 0;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    for(int i = 1; i <= n; i++) {
        for(int j = i+1; j <= n; j++) { // consider all pairs (i < j)
            int andVal = i & j;
            int orVal = i | j;
            int xorVal = i ^ j;

            if(andVal > maxAnd)
                maxAnd = andVal;
            if(orVal > maxOr)
                maxOr = orVal;
            if(xorVal > maxXor)
                maxXor = xorVal;
        }
    }

    printf("Maximum AND value: %d\n", maxAnd);
    printf("Maximum OR value: %d\n", maxOr);
    printf("Maximum XOR value: %d\n", maxXor);

    return 0;
}
```
Output:
<img width="1527" height="668" alt="image" src="https://github.com/user-attachments/assets/b2c8821b-253f-486a-9e1c-1ede3f932dd8" />

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>

int main() {
    int noshel, noque;

    // Step 2: Input number of shelves and queries
    printf("Enter number of shelves and number of queries: ");
    scanf("%d %d", &noshel, &noque);

    int shelarr[noshel][100];   // Assuming max 100 books per shelf
    int nobookarr[noshel];      // Number of books on each shelf
    int i, j, k, c;

    // Initialize number of books on each shelf
    for(i = 0; i < noshel; i++)
        nobookarr[i] = 0;

    // Process queries
    for(i = 0; i < noque; i++) {
        int type;
        printf("\nEnter query type (1: Add book, 2: Count books on shelf, 3: Get book ID): ");
        scanf("%d", &type);

        if(type == 1) {
            int shelf, bookID;
            printf("Enter shelf number and book ID to add: ");
            scanf("%d %d", &shelf, &bookID);
            shelarr[shelf][nobookarr[shelf]] = bookID;
            nobookarr[shelf]++;
        } 
        else if(type == 2) {
            int shelf;
            printf("Enter shelf number to count books: ");
            scanf("%d", &shelf);
            printf("Number of books on shelf %d: %d\n", shelf, nobookarr[shelf]);
        } 
        else if(type == 3) {
            int shelf, index;
            printf("Enter shelf number and book index: ");
            scanf("%d %d", &shelf, &index);
            if(index < nobookarr[shelf])
                printf("Book ID at shelf %d, index %d: %d\n", shelf, index, shelarr[shelf][index]);
            else
                printf("Invalid index!\n");
        } 
        else {
            printf("Invalid query type!\n");
        }
    }

    return 0;
}
```
Output:
<img width="1591" height="706" alt="image" src="https://github.com/user-attachments/assets/f30082e1-7bdc-4569-8209-531b4ff6a1c5" />

Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the number of elements in the array: ");
    scanf("%d", &n);

    int arr[n];

    printf("Enter %d integers: ", n);
    for(int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        sum += arr[i];  // Add each element to sum
    }

    printf("Sum of the integers in the array: %d\n", sum);

    return 0;
}
```

Output:
<img width="1467" height="656" alt="image" src="https://github.com/user-attachments/assets/89e644e0-4bc4-49f8-af6a-11a66f781fc7" />

Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char sentence[1000];
    int count = 0;

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);

    int inWord = 0; // Flag to check if inside a word
    for(int i = 0; sentence[i] != '\0'; i++) {
        if(!isspace(sentence[i]) && !inWord) {
            inWord = 1;
            count++;
        } else if(isspace(sentence[i])) {
            inWord = 0;
        }
    }

    printf("Number of words in the sentence: %d\n", count);

    return 0;
}
```
Output:
<img width="1432" height="641" alt="image" src="https://github.com/user-attachments/assets/5fd52d4b-1efd-42f6-b50d-8a714ed0e402" />

Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
