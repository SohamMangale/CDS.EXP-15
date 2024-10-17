# EXPERIMENT - 15
## AIM :
To study and implement recursion.

## THEORY :
A recursive function solves a particular problem by calling a copy of itself and solving smaller subproblems of the original problems. Many more recursive calls can be generated as and when required. It is essential to know that we should provide a certain case in order to terminate this recursion process. So we can say that every time the function calls itself with a simpler version of the original problem.

## Key Components of Recursion :
### Base Case:

The condition that terminates the recursion.
Prevents infinite recursion by stopping further recursive calls.
Recursive Case:

The part of the function that makes a call to itself.
Solves a smaller or simpler instance of the problem.
How Recursion Works:
### Function Call:

When the function calls itself, it pauses execution.
### Recursive Call:

The function makes a new call with modified arguments (typically smaller or simpler).
### Resume Execution:

Once the base case is met, paused calls resume from where they left off.
The function then returns the result back through the call stack.
### Memory allotment :
When any function is called from main(), the memory is allocated to it on the stack. A recursive function calls itself, the memory for a called function is allocated on top of memory allocated to the calling function and a different copy of local variables is created for each function call.
## Codes
### 1. Factorial
~~~
//soham
//entc B1
//23070123084
//experiment 15
#include<iostream>
using namespace std;
//create function 
int fact(int n)
{
    if(n<=1)
    {
        return 1;
}else
{
    return (n*fact(n-1));
}
}
int main()
{
    int x,n;
    cout<<"enter a number: ";
    cin>>n;
    x = fact(n);
    cout<<n<<"! = "<<x;
    return 0;
}
~~~
### 2. Addition
~~~
//soham
//entc B1
//23070123084
//experiment 15A
#include<iostream>
using namespace std;
//create function 
int add(int n)
{
    if(n<=1)//base condition
    {
        return 1;
}else
{
    return (n+add(n-1));//recursion
}
}
int main()
{
    int x,n;
    cout<<"enter a number: ";
    cin>>n;
    x = add (n);//function calling
    cout<<n<<"+ = "<<x;
    return 0;
}
~~~
### 3. Reverse Of A String
//soham
//entc B1
//23070123084
//experiment 15B
#include<iostream>
using namespace std;
//create function 
int add(int n)
{
    if(n<=1)//base condition
    {
        return 1;
}else
{
    return (n+add(n-1));//recursion
}
}
int main()
{
    int x,n;
    cout<<"enter a number: ";
    cin>>n;
    x = add (n);//function calling
    cout<<n<<"+ = "<<x;
    return 0;
}
~~~
### 4. Reverse Of A Integer
~~~
//soham
//entc B1
//23070123084
//experiment 15C
#include <iostream>
using namespace std;

void print_rev(int i)
{
    if (i > 0)
    {
        cout << (i % 10);
        print_rev(i / 10);//recursion
    }
}

int main()
{
    int i;
    cout << "Enter a Number: ";
    cin >> i;
    print_rev(i); // Function calling
    return 0;
}
~~~
## Outputs :
### 1. Factorial
Screenshot 2024-09-13 113925

### 2. Addition
Screenshot 2024-09-13 113950

### 3. Reverse Of A String
Screenshot 2024-09-13 114125

### 4. Reverse Of A Integer
Screenshot 2024-09-13 114633

## Conclusion :
We effectively studied and implemented the idea of recursion in C++ in this experiment. Examples of recursion, which is the process by which a function calls itself to solve smaller sub-problems, included finding the factorial, creating Fibonacci sequences, and searching algorithms. By examining recursive functions, we discovered the following important realizations:

Simpleness of Expression: When a problem is inherently recursive, such as in the case of tree traversal and divide-and-conquer algorithms, recursive solutions frequently offer a clear and simple approach to solve it.
Base Case and Termination: In the absence of suitable ending circumstances, unbounded recursion and stack overflow result. This highlights the significance of having a well-defined base case.
Stack Depth and Limitations: We also discovered that recursive methods may not be suitable for solving some problems due to the possibility of stack overflow errors resulting from deep recursion
