#include <stdio.h>

#define MAX_SIZE 100

int arr[MAX_SIZE];
int size = 0;

void insert(int element, int position) {
    if (position < 0 || position > size) {
        printf("Invalid position\n");
        return;
    }
    for (int i = size - 1; i >= position; i--) {
        arr[i + 1] = arr[i];
    }
    arr[position] = element;
    size++;
}

void delete(int position) {
    if (position < 0 || position >= size) {
        printf("Invalid position\n");
        return;
    }
    for (int i = position; i < size - 1; i++) {
        arr[i] = arr[i + 1];
    }
    size--;
}

void display() {
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int main() {
    insert(10, 0);
    insert(20, 1);
    insert(30, 2);
    insert(5, 0);

    printf("Array after insertion: ");
    display();
    delete(2);

    printf("Array after deletion: ");
    display();

    return 0;
}
