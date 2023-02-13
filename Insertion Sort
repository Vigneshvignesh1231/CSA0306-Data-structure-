#include <stdio.h>

void insertionSort(int array[], int n) {
    int i, j, temp;
    for (i = 1; i < n; i++) {
        temp = array[i];
        j = i - 1;
        while (j >= 0 && array[j] > temp) {
            array[j + 1] = array[j];
            j--;
        }
        array[j + 1] = temp;
    }
}

int main() {
    int array[] = {5, 2, 9, 1, 5, 6},i;
    int n = sizeof(array) / sizeof(array[0]);

    printf("Unsorted array: \n");
    for (i = 0; i < n; i++)
        printf("%d ", array[i]);

    insertionSort(array, n);

    printf("\nSorted array: \n");
    for (i = 0; i < n; i++)
        printf("%d ", array[i]);

    return 0;
}
