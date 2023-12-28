Non Repeating Element in an array in C
Here, in this page we will discuss the program to print print non repeating element in an array in C programming language. We are given with an array and need to print the unique elements, means those which have frequency one.

Distinct elements in C
Method (Using loops) :
In this method we will count the frequency of each elements using two for loops, and whose frequency will be 1 then print that element.

To check the status of visited elements create a array of size n.
Run a loop from index 0 to n and check if (visited[i]==1) then skip that element.
Otherwise create a variable count = 1 to keep the count of frequency.
Run a loop from index i+1 to n
Check if(arr[i]==arr[j]), then increment the count by 1 and set visited[j]=1.
After complete iteration of inner for loop, check if(count==1), if it is then print that ith element.
Time and Space Complexity:
Time Complexity : O(n2)
Space Complexity : O(n), as we declare an extra array to keep track the visited element of the array.
Distinct element in an array using C
In this method we first count the frequency of each elements, so to know more about the algorithm for finding the frequency of elements of the array. You can check out the page given below,

Related Pages
Counting Distinct Elements in an Array

Finding  Repeating elements in an Array

Removing Duplicate elements from an array

Finding Minimum scalar product of two vectors

Finding Maximum scalar product of two vectors in an array 

C Program to Count the Frequency
Code in C
Run
#include <stdio.h>

// Main function to run the program
int main() 
{ 
    int arr[] = {21, 30, 10, 2, 10, 20, 30, 11}; 
    int n = sizeof(arr)/sizeof(arr[0]); 

    int visited[n];
 
    for(int i=0; i<n; i++){

       if(visited[i]==0){
          int count = 1;
          for(int j=i+1; j<n; j++){
             if(arr[i]==arr[j]){
                count++;
                visited[j]=1;
             }
          }
         if(count==1)
          printf("%d ",arr[i]);
       }
   }
   
   return 0; 
}
Output
21 2 20 11
