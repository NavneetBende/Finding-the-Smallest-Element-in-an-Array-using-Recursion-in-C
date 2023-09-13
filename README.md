# Finding-the-Smallest-Element-in-an-Array-using-Recursion-in-C

Find the Smallest Element in an Array using Recursion in C
Given the length of the array “n” and the array itself “A”, Find the Smallest Element in an Array using Recursion in C Language.

For instance,

Input: A = [1, 4, 3, -5, -4, 8, 6]
Output: -5
Find the Smallest Element in an Array using Recursion in C
Find the Smallest Element in an Array using Recursion 
the objective of the program is to recursively traverse through the string while comparing the elements. If the element is Smaller than the previous one. update the Smallest variable until no other element is Smaller than it. To do so we can use either recursion or iteration. We’ll use iteration on this page, the link to solutions with other approaches is given at the end of the page. 

Lets try and understand using an example. an Array A = [ 10, 324, 45 ].  Declare a function with the base case as when n==1 we return the first character of the array. The recursive function returns the minimum of the last element of the array passed as an argument and the returned value from the recursion. The recursion process is shown in the image adjacent. When in the last block the base case is satisfied, first element of the array is returned. The output is 10.

Find the Smallest Element using Recursion in C
While loop in C
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Largest element in an array

Power of a Number

Prime Number

C Code
Run
#include <stdio.h>

int min(int a, int b)
{
    return a>b?b:a ;
}

int findMinRec(int A[], int n)
{
    if (n == 1)
        return A[0];
    return min(A[n-1], findMinRec(A, n-1));
}
int main()
{
    int arr[] = {10, 324, 45, 90, 9808};
    int n = sizeof(arr)/sizeof(arr[0]);
    printf("Smallest in given array is %d", findMinRec(arr, n));
    return 0;
}
Output
Smallest in given array is 10
Explanation

The objective of the code is to recursively parse through the array input while checking for the smallest element in the array. To do so we call recursively and break down the string into tiny strings. 

The algorithm for the above C code is as follows,

 Include the Required Library.
Define min() function which takes two integer variables and return the smallest among the two.
Declare findMinRec() function that takes the array and it’s length as arguments.
Set base case as n==1, if true return the first element of the array A.
else return the minimum value of the last element of the array A and the value returned by the recursive call of the function using min() function.
In the int main() function declare and initialize the variables and call the findMinRec() function. 
Print the result using printf() function.
The output for the above code is the smallest element in the Array input i.e 10.
