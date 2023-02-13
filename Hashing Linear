#include <stdio.h>
#include <stdlib.h>

#define SIZE 10

int hashTable[SIZE];

void init() {
	int i;
    for (i = 0; i < SIZE; i++) {
        hashTable[i] = -1;
    }
}

int hashFunction(int key) {
    return key % SIZE;
}

void insert(int key) {
    int index = hashFunction(key);
    if (hashTable[index] != -1) {
        int i = (index + 1) % SIZE;
        while (i != index) {
            if (hashTable[i] == -1) {
                hashTable[i] = key;
                return;
            }
            i = (i + 1) % SIZE;
        }
    } else {
        hashTable[index] = key;
    }
}

void search(int key) {
    int index = hashFunction(key);
    if (hashTable[index] == key) {
        printf("Key found at index %d\n", index);
        return;
    }
    int i = (index + 1) % SIZE;
    while (i != index) {
        if (hashTable[i] == key) {
            printf("Key found at index %d\n", i);
            return;
        }
        i = (i + 1) % SIZE;
    }
    printf("Key not found\n");
}

int main() {
    init();
    insert(1);
    insert(2);
    insert(3);
    insert(4);
    search(3);
    search(5);
    return 0;
}
