# Recursion
Experiment 15

## Aim 
To study Recursion

## Theory
### Definition
#### What is a Recursion?
- Recursion in C++ is a technique where a function calls itself to solve a problem.
- This approach is often used for problems that can be divided into smaller, similar subproblems. 
- A recursive function typically has two main components:
  - Base Case: A condition under which the function will stop calling itself, preventing 
  infinite recursion.
  - Recursive Case: The part of the function where it calls itself with modified arguments to 
  gradually approach the base case.
> For example:
```cpp
#include<iostream>
using namespace std;

int fact(int n)
{
    if (n<=1)
        return 1;

    else return (n*fact(n-1));
}
int main()
{
    int a;
    cout<<"Enter an integer: "<<endl;
    cin>>a;
    cout<<"Factorial is: "<<fact(a);
}
```

## Algorithms
1. Start
2. Input an integer `a`
3. Function Definition (`fact(n)`):
    - If `n <= 1`, return 1 (base case)
    - Else, return `n * fact(n - 1)` (recursive case)
4. Call the function `fact(a)` to calculate the factorial of the number:
    - If `a` is 0 or 1, factorial is 1.
    - Otherwise, multiply `a` with the factorial of `a - 1` and keep repeating this process until `a` becomes 1 (recursive breakdown).
5. Output the result of the factorial.
6. End

Example walkthrough for `fact(5)`:   
`fact(5)` → returns `5 * fact(4)`   
`fact(4)` → returns `4 * fact(3)`   
`fact(3)` → returns `3 * fact(2)`   
`fact(2)` → returns `2 * fact(1)`   
`fact(1)` → returns `1`   
Final result: `5 * 4 * 3 * 2 * 1 = 120`.
