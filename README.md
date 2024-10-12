# Experiment-17

### AIM
To study and implement stack implementation using array.

### Problem Statement
1.) Write a c++ program to do stack implementation.

# Theory
A stack is a data structure that works on a Last In, First Out (LIFO) principle, meaning the last item you add is the first one you take away. You can add items to the top (called "pushing") and take items off the top (called "popping"), and you can also check what's on top or see if the stack is empty. Stacks can be built using arrays or linked lists and are often used in situations like undo features in text editors and keeping track of function calls, providing flexibility through dynamic memory use.

### Program Code

```javascript
//Mohit Singh Rawat
//23070123086
#include <iostream>
using namespace std;
#define size 5
#define ERROR -9999
class Stack{
    int top, ar[size];
    public:
    Stack()
    {
        top=-1;
        ar[0]=0;
    }
    void push(int);
    int pop();
    int peak();
    void disp();
};
void Stack::push(int num)
{
    if (top==size-1)
    {
        cout<<"STACK OVERFLOW: Stack is full"<<endl;
        return;
    }
    else
    {
        ar[++top]=num;
    }
}
int Stack::pop()
{
    int val;
    if(top==-1)
    {
        cout<<"STACK UNDERFLOW: STACK IS EMPTY"<<endl;
        return ERROR;
    }
    else{
         val=ar[top--];
         return val;
    }
}
int Stack::peak()
{
    if(top==-1)
    {
        cout<<"STACK UNDERFLOW: stack is empty"<<endl;
        return ERROR;
    }
    else
    {
        return ar[top];
    }
}
void Stack::disp()
{
    if(top==-1)
    {
       cout<<"STACK UNDERFLOW: stack is empty"<<endl;
        return ;
    }
    else
    {
        int i=0;
        while(i!=(top+1))
        {
            cout<<ar[i]<<"  ";
            i++;
        }
    }
}
int main()
{
    Stack s1;
    s1.push(7);
    s1.push(10);
    s1.push(4);
    int val=s1.pop();
    cout<<val;
    int top=s1.peak();
    cout<<top;
    s1.disp();
    return 0;
}
```

### Program Output

![image](https://github.com/user-attachments/assets/f9f919fe-795b-4e75-8c81-3e2e2f36a0ae)

### Conclusion
In conclusion, stacks are important data structures that help organize and manage data in a specific way. They are useful in many programming tasks and applications where keeping data in a clear and predictable order is needed.




