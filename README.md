# Stack-Implementation-in-Cpp
# Name: Rajeev Raesh Reddy E
# PRN: 24070123081

Aim: To study and implement the concept of Stack in C++ using arrays and functions with operations such as PUSH, POP, and PEEK.

Software used: Vs Code

Theory: 

A stack is a linear data structure in C++ that follows the Last-In-First-Out (LIFO) principle. Using arrays and functions, stack operations like PUSH (insert), POP (remove), and PEEK (view top element) can be implemented efficiently. The stack uses a `top` pointer to track the current position. It’s ideal for problems involving recursion, expression evaluation, and backtracking. Understanding stack logic strengthens grasp over memory management and control flow in algorithmic programming.


Syntax:

    #include <iostream>
    using namespace std;

    #define SIZE 100  // Maximum size of stack

    class Stack {
    int arr[SIZE];
    int top;

    public:
    Stack() {
        top = -1;
    }

    // PUSH operation
    void push(int value) {
        if (top >= SIZE - 1)
            cout << "Stack Overflow\n";
        else
            arr[++top] = value;
    }

    // POP operation
    void pop() {
        if (top < 0)
            cout << "Stack Underflow\n";
        else
            top--;
    }

    // PEEK operation
    void peek() {
        if (top < 0)
            cout << "Stack is Empty\n";
        else
            cout << "Top element: " << arr[top] << endl;
    }

    // Display stack
    void display() {
        if (top < 0)
            cout << "Stack is Empty\n";
        else {
            cout << "Stack elements: ";
            for (int i = top; i >= 0; i--)
                cout << arr[i] << " ";
            cout << endl;
        }
    }
    };

    int main() {
    Stack s;
    s.push(10);
    s.push(20);
    s.peek();
    s.pop();
    s.display();

    return 0;
    }


Algorithm:

i) Algorithm: Stack Implementation Using Arrays in C++

 1. Define Stack Class
- Create a class `Stack` with:
  - An integer array `arr[SIZE]` to store stack elements.
  - An integer `top` to track the top index, initialized to -1.

 2. Implement Stack Operations
- `push(int value)`: Adds an element to the top if not full; else shows overflow.
- `pop()`: Removes the top element if not empty; else shows underflow.
- `display()`: Prints all elements from top to bottom.

 3. Menu-Driven Interface
- In `main()`, use a loop to present options:
  - 1 for push, 2 for pop, 3 for display, 0 to exit.

 4. Handle User Input
- Use `cin` to take user choice and value (for push).
- Call corresponding stack methods based on the choice.

 5. Exit Program
- Continue loop until user selects option 0.
- Display exit message and return 0 to end execution.

Conclusion:

This program demonstrates stack implementation in C++ using arrays and functions, reinforcing core operations like PUSH, POP, and DISPLAY. It highlights the Last-In-First-Out (LIFO) principle and shows how to manage overflow and underflow conditions. Such structured logic builds a strong foundation for mastering data structures and algorithmic thinking.
