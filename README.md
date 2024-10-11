# Stack-Implementation-using-array
# Stack Implementation in C++ using Dynamic Array

## Overview

This project demonstrates a simple stack data structure implementation in C++ using dynamic arrays. The stack supports the following operations:

- **Push**: Add an element to the top of the stack.
- **Pop**: Remove the top element from the stack.
- **Peek**: View the top element of the stack without removing it.

## Features

1. **Dynamic Memory Allocation**: The stack is implemented using a dynamic array to allocate memory based on the user-defined stack size.
2. **Basic Operations**:
   - **Push**: Adds an element to the top of the stack.
   - **Pop**: Removes the top element from the stack.
   - **Peek**: Retrieves the top element without removing it.
3. **Memory Management**: The stack dynamically allocates memory during initialization and frees it upon destruction to prevent memory leaks.

## Code Explanation

### `Stack` Class

#### Attributes:
- `int capacity`: The maximum size of the stack.
- `int top`: Tracks the current top element of the stack (initially -1).
- `int* arr`: A pointer to dynamically allocated memory for the stack.

#### Methods:
- **Constructor**: Allocates memory for the stack based on the capacity passed as a parameter.
- **Destructor**: Deallocates the dynamically allocated memory for the stack.
- **push(int element)**: Adds an element to the stack if it is not full; otherwise, it prints a "Stack Overflow" message.
- **pop()**: Removes the top element from the stack if it is not empty; otherwise, it prints a "Stack Underflow" message.
- **peek()**: Returns the top element of the stack if it is not empty. Returns `-1` if the stack is empty.

### Example Usage (in `main()` function)

In this example, we:
1. Create a stack with a capacity of 5.
2. Push three integers (`23`, `24`, `25`) onto the stack.
3. Use the `peek()` method to get the top element of the stack.
4. Pop the top element and then peek again to view the new top element.

```cpp
int main() {
    Stack st(5);
    st.push(23);
    st.push(24);
    st.push(25);

    cout << st.peek() << endl; // Output: 25
    st.pop();
    cout << st.peek() << endl; // Output: 24

    return 0;
}
```

### Sample Output

```
25
24
```

## How to Run

1. Copy the provided code into a C++ file (e.g., `stack.cpp`).
2. Compile the file using a C++ compiler. For example:
   ```
   g++ -o stack stack.cpp
   ```
3. Run the executable:
   ```
   ./stack
   ```

## Notes

- **Stack Overflow**: Occurs when you try to push an element onto the stack when it's already full.
- **Stack Underflow**: Occurs when you try to pop an element from an empty stack.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

--- 
