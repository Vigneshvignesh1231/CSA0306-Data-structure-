#include <stdio.h>
#define MAX 5
int queue[MAX], front = -1, rear = -1;
void enqueue() {
    int data;
    if (rear == MAX - 1) {
        printf("Queue is full\n");
    } else {
        printf("Enter data to be inserted : ");
        scanf("%d", &data);
        if (front == -1) {
            front = 0;
        }
        rear++;
        queue[rear] = data;
    }
}
void dequeue() {
    if (front == -1) {
        printf("Queue is empty\n");
    } else {
        printf("Deleted element is : %d\n", queue[front]);
        front++;
        if (front > rear) {
            front = rear = -1;
        }
    }
}

void display() {
    if (rear == -1) {
        printf("Queue is empty\n");
    } else {
        int i;
        printf("Queue elements are : ");
        for (i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }
}

int main() {
    int choice;
    while (1) {
        printf("1. Insert element to queue\n");
        printf("2. Delete element from queue\n");
        printf("3. Display all elements of queue\n");
        printf("4. Exit\n");
        printf("Enter your choice : ");
        scanf("%d", &choice);
        switch (choice) {
            case 1:
                enqueue();
                break;
            case 2:
                dequeue();
                break;
            case 3:
                display();
                break;
            case 4:
                exit(0);
            default:
                printf("Wrong choice\n");
        }
    }
    return 0;
}
