#include <stdio.h>
#define MAX_SIZE 100 

int a[MAX_SIZE];
int size = 0;

void insert(int element, int pos) {
  if (size == MAX_SIZE) {
    printf("Array is full\n");
  } else if (pos < 0 || pos > size) {
    printf("Invalid position\n");
  } else {
    for (int i = size - 1; i >= pos; i--) {
      a[i+1] = a[i];
    }
    a[pos] = element;
    size++;
  }
}

void delete(int pos) {
  if (size == 0) {
    printf("Array is empty\n");
  } else if (pos < 0 || pos >= size) {
    printf("Invalid position\n");
  } else {
    for (int i = pos; i < size - 1; i++) {
      a[i] = a[i + 1];
    }
    size--;
  }
}

void display() {
  if (size == 0) {
    printf("Array is empty\n");
  } else {
    for (int i = 0; i < size; i++) {
      printf("%d ", a[i]);
    }
    printf("\n");
  }
}

int main() {
  insert(1, 0);
  insert(2, 1);
  insert(3, 2);
  display();
  delete(1);
  display();
  return 0;
}
