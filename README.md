## EXPERIMENT-25-SHIFT OPERATIONS

### AIM:
To create a program that performs left and right shift operations on an unsigned integer and prints the results.

### ALGORITHM:
1. Begin the program.
2. Declare a variable `a` of type unsigned int to store the input value.
3. Prompt the user to input a value for `a`.
4. Read the input value for `a` using `scanf()` function.
5. Declare a variable `c` of type int to store the result of shift operations.
6. Perform a left shift operation on `a` by 2 bits and store the result in `c`.
7. Print the result of the left shift operation.
8. Perform a right shift operation on `a` by 2 bits and store the result in `c`.
9. Print the result of the right shift operation.
10. End the program.
## PROGRAM:
``` 
#include <stdio.h>
int main() {
    unsigned int a ;	/* 60 = 0011 1100 */  
    scanf("%u",&a);
      int c = 0; 
    c = a << 2;     /* 240 = 1111 0000 */
   printf("After Left Shift Operation value of a is:%d\n", c );
   c = a >> 2;     /* 15 = 0000 1111 */
   printf("After Right Shift Operation value of a is:%d\n", c );
}
```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/688d9d99-9fb8-4c08-9184-a12617a16fd5)


## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/ccd0b2cd-69a3-4bd0-ad79-2b4586b5c353)



## RESULT:
Thus the required program is written and executed successfully.



## EXPERIMENT-26-CURRENCY BREAKDOWN

### AIM:
To develop a program that calculates and prints the breakdown of an amount into various currency denominations.

### ALGORITHM:
1. Begin the program.
2. Declare variables `amt` and `total` of type int to store the input amount and the number of currency notes.
3. Prompt the user to input the amount.
4. Read the input value for `amt` using `scanf()` function.
5. Calculate the number of 20.00 currency notes by dividing `amt` by 20 and store the result in `total`.
6. Print the number of 20.00 currency notes.
7. Update `amt` by subtracting the total value of 20.00 currency notes.
8. Repeat steps 5-7 for 10.00, 5.00, 2.00, and 1.00 currency denominations.
9. End the program.
## PROGRAM:
``` 
#include<stdio.h> 
int main() 
{ 
     /* Move p1'th to rightmost side */
    unsigned int n,p1=2,p2=4;
    scanf("%ud",&n);
    unsigned int bit1 =  (n >> p1) & 1; 
  
    /* Move p2'th to rightmost side */
    unsigned int bit2 =  (n >> p2) & 1; 
  
    /* XOR the two bits */
    unsigned int x = (bit1 ^ bit2); 
  
    /* Put the xor bit back to their original positions */
    x = (x << p1) | (x << p2); 
  
    /* XOR 'x' with the original number so that the two sets are swapped */
    unsigned int res = n ^ x; 
    printf("Result = %d ", res); 
    return 0; 
} 

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/0f468ad8-bc83-4eee-b087-3a064df3b29a)


## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/57913a2a-e376-499f-9ad9-7e49426a21f6)



## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-27-TRIANGLE VALIDATOR

### AIM:
To develop a program that determines whether a triangle with given side lengths is valid or not.

### ALGORITHM:
1. Begin the program.
2. Declare variables `side1`, `side2`, and `side3` of type float to store the lengths of the sides of the triangle.
3. Prompt the user to input the lengths of the three sides of the triangle.
4. Read the input values for `side1`, `side2`, and `side3` using `scanf()` function.
5. Use nested if-else statements to check if the triangle is valid:
   - Check if the sum of any two sides is greater than the third side.
   - If all three conditions are true, print "Triangle is valid".
   - Otherwise, print "Triangle is not valid".
6. End the program.

## PROGRAM:
``` 
#include <stdio.h>

int main() {
    float side1, side2, side3;
    scanf("%f", &side1);
    scanf("%f", &side2);
    scanf("%f", &side3);

    // Check if the triangle is valid using nested if-else
    if (side1 + side2 > side3) {
        if (side1 + side3 > side2) {
            if (side2 + side3 > side1) {
                printf("Triangle is valid.\n");
            } else {
                printf("Triangle is not valid.\n");
            }
        } else {
            printf("Triangle is not valid.\n");
        }
    } else {
        printf("Triangle is not valid.\n");
    }

    return 0;
}


```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/32e2d65a-ae03-46ad-8fea-abea8bea97e2)



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/1cc4346d-646a-4a53-8656-8415af4726cf)




## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-28-WIND SPEED CLASSIFIER

### AIM:
To create a program that classifies wind speed into different categories based on predefined ranges.

### ALGORITHM:
1. Begin the program.
2. Declare a variable `windSpeed` of type float to store the input wind speed.
3. Prompt the user to input the wind speed.
4. Read the input value for `windSpeed` using `scanf()` function.
5. Use if-else statements to classify the wind speed into different categories based on predefined ranges:
   - If `windSpeed` is between 39 and 49, print "Strong breeze".
   - If `windSpeed` is between 50 and 61, print "Moderate gale".
   - If `windSpeed` is between 62 and 74, print "Fresh gale".
   - If `windSpeed` is between 75 and 97, print "Moderate gale".
   - If `windSpeed` is greater than 98, print "Strong gale".
   - If none of the above conditions are met, print "Wind speed is not within the specified ranges."
6. End the program.

## PROGRAM:
``` 
#include <stdio.h>

int main() {
    float windSpeed;
    scanf("%f", &windSpeed);

    // Check the wind speed and display the appropriate message
    if (windSpeed >= 39 && windSpeed <= 49) {
        printf("Strong breeze\n");
    } else if (windSpeed >= 50 && windSpeed <= 61) {
        printf("Moderate gale\n");
    } else if (windSpeed >= 62 && windSpeed <= 74) {
        printf("Fresh gale\n");
    } else if (windSpeed >= 75 && windSpeed <98) {
        printf("Moderate gale\n");
    }
    else if (windSpeed > 98) {
        printf("Strong gale\n");
    } else {
        printf("Wind speed is not within the specified ranges.\n");
    }

    return 0;
}


```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/a01fc86b-bc24-43d5-a145-b539b7ea3bd3)




## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/71e76d5e-f925-4d3d-9bbd-5372b27feabb)




## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-29-STRING LENGTH CALCULATOR

### AIM:
To create a program that calculates and prints the length of a given string.

### ALGORITHM:
1. Begin the program.
2. Declare a character array `str` of size 100 to store the input string.
3. Declare an integer variable `length` to store the length of the string.
4. Prompt the user to input a string.
5. Read the input string into the array `str` using `scanf()` function.
6. Calculate the length of the string using the `strlen()` function and store the result in the variable `length`.
7. Print the length of the string.
8. End the program.

## PROGRAM:
``` 
#include <stdio.h>
#include <string.h>

int main() {
    char str[100]; 
    int length;
    scanf("%s", str); 

    // Find the length of the string
    length = strlen(str);

    // Print the length of the string
    printf("Length of Str is %d\n", length);

    return 0;
}

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/7ebef428-7c21-484d-9aba-f278c9752054)



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/bafb3670-208f-4e2f-84fc-fb399aab7416)



## RESULT:
Thus the required program is written and executed successfully.



## EXPERIMENT-30-TITLE CASE CONVERTER

### AIM:
To develop a program that converts the first character of each word in a given string to uppercase.

### ALGORITHM:
1. Begin the program.
2. Declare a character array `str` of size 30 to store the input string.
3. Prompt the user to input a string containing spaces.
4. Read the input string into the array `str` using `scanf()` function, allowing spaces with `%[^\n]` format specifier.
5. Iterate through each character of the string using a for loop:
   - If the current character is the first character of the string or the character immediately following a space, convert it to uppercase using `toupper()` function.
   - If the next character is a space or the end of the string, convert the current character to uppercase.
6. Print the converted string.
7. End the program.

## PROGRAM:
``` 
#include <stdio.h>
#include <ctype.h>
#include <string.h>
int main()
{
    char str[30];
    scanf("%[^\n]",str);
    int i=0;
    for(i=0;i<strlen(str);i++)
    {
        if(i==0||str[i-1]==' ')
        {
            str[i]=toupper(str[i]);
        }
        else if(str[i+1]==' '||str[i+1]=='\0')
        {
            str[i]=toupper(str[i]);
        }
    }
    printf("After Converting String is:%s",str);
}
```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/3f36ff77-fc38-473c-b588-540407b8d50f)


## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/cc2f6371-8a70-4ba8-bfef-811fc5c904df)



## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-31-STRING WORD SPLITTER

### AIM:
To develop a program that splits a given string into individual words separated by spaces and prints each word on a new line.

### ALGORITHM:
1. Begin the program.
2. Declare two character arrays `str` and `word` of size 100 to store the input string and individual words respectively.
3. Declare two integer variables `i` and `j` to use as loop indices.
4. Prompt the user to input a string.
5. Read the input string into the array `str` using `fgets()` function to allow input with spaces.
6. Print a message indicating the words after splitting by space.
7. Iterate through each character in the string using a while loop:
   - If the current character is not a space, add it to the current word in the array `word`.
   - If the current character is a space:
     - Null-terminate the current word in the array `word`.
     - Print the current word.
     - Reset the index `j` to 0 to prepare for the next word.
8. Print the last word if the string does not end with a space.
9. End the program.

## PROGRAM:
``` 
#include <stdio.h>

int main() {
    char str[100];
    char word[100];
    int i = 0, j = 0;

    printf("Enter a string: \n");
    fgets(str, sizeof(str), stdin); // Read the string

    printf("Words after split by space are:\n");

    // Iterate through each character in the string
    while (str[i] != '\0') {
        // If the character is not a space, add it to the current word
        if (str[i] != ' ') {
            word[j] = str[i];
            j++;
        } else {
            // If the character is a space, print the current word and reset for the next word
            word[j] = '\0'; // Null-terminate the word
            printf("%s\n", word);
            j = 0; // Reset the word index
        }
        i++;
    }

    // Print the last word if the string does not end with a space
    if (j > 0) {
        word[j] = '\0'; // Null-terminate the last word
        printf("%s\n", word);
    }

    return 0;
}

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/25c71c3e-e10b-42c7-8a40-f5821ae6b012)



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/ffcb533c-6ec1-4979-9fac-b83ccc0917e2)



## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-32-UPPERCASE CONVERTER

### AIM:
To create a program that converts all lowercase characters in a given string to uppercase.

### ALGORITHM:
1. Begin the program.
2. Declare a character array `a` of size 30 to store the input string.
3. Prompt the user to input a string.
4. Read the input string into the array `a` using `fgets()` function.
5. Iterate through each character in the string using a for loop:
   - Check if the current character is a lowercase letter (i.e., between 'a' and 'z').
   - If it is, convert it to uppercase by subtracting 32 from its ASCII value.
6. Print the converted string.
7. End the program.
## PROGRAM:
``` 
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main(){
    char a[30];
    fgets(a,30,stdin);
    
    for(int i=0;i<strlen(a);i++)
    {
       if(a[i]>='a' && a[i]<='z')
            a[i]=a[i]-32;
    }
    printf("%s",a);
    
}
```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/dc7d6dd7-e8e2-43a5-bd04-65ef3247a3f7)



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-4/assets/144870412/6890c645-0180-4df8-8113-d63db4bfe2e9)




## RESULT:
Thus the required program is written and executed successfully.



















