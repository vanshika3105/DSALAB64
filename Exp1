Code:

#include <stdio.h>
#include <stdlib.h>

#define MAX 10 // Maximum size of the stack

int stack[MAX]; // Array to hold stack elements
int top = -1; // Initialize top of the stack

// Function prototypes
void push(int item);
int pop();
void display();
int isEmpty();
int isFull();

int main() {
    int choice, item;

    while (1) {
        printf("\nStack Operations Menu:");
        printf("\n1. Push");
        printf("\n2. Pop");
        printf("\n3. Display");
        printf("\n4. Check if Empty");
        printf("\n5. Check if Full");
        printf("\n6. Exit");
        printf("\nEnter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter an element to push: ");
                scanf("%d", &item);
                push(item);
                break;
            case 2:
                item = pop();
                if (item != -1) {
                    printf("Popped element: %d\n", item);
                }
                break;
            case 3:
                display();
                break;
            case 4:
                if (isEmpty()) {
                    printf("Stack is empty.\n");
                } else {
                    printf("Stack is not empty.\n");
                }
                break;
            case 5:
                if (isFull()) {
                    printf("Stack is full.\n");
                } else {
                    printf("Stack is not full.\n");
                }
                break;
            case 6:
                exit(0);
            default:
                printf("Invalid choice! Please enter a valid option.\n");
        }
    }
    return 0;
}

void push(int item) {
    if (isFull()) {
        printf("Stack Overflow! Cannot push %d\n", item);
    } else {
        stack[++top] = item; // Increment top and add item
        printf("Pushed %d onto the stack.\n", item);
    }
}

int pop() {
    if (isEmpty()) {
        printf("Stack Underflow! Cannot pop from an empty stack.\n");
        return -1; // Return -1 to indicate underflow
    } else {
        return stack[top--]; // Return top element and decrement top
    }
}

void display() {
    if (isEmpty()) {
        printf("Stack is empty.\n");
    } else {
        printf("Stack elements are:\n");
        for (int i = top; i >= 0; i--) {
            printf("%d\n", stack[i]);
        }
    }
}

int isEmpty() {
    return top == -1; // Returns 1 if empty, otherwise 0
}

int isFull() {
    return top == MAX - 1; // Returns 1 if full, otherwise 0
}
