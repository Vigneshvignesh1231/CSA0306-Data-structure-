#include <stdio.h>

int binarySearch(int arr[], int left, int right, int x) {
    if (right >= left) {
        int mid = left + (right - left) / 2;

        if (arr[mid] == x) {
            return mid;
        }

        if (arr[mid] > x) {
            return binarySearch(arr, left, mid - 1, x);
        }

        return binarySearch(arr, mid + 1, right, x);
    }

    return -1;
}

int main() {
    int arr[] = {1, 4, 6, 8, 9, 11, 14, 15, 20, 25};
    int size = sizeof(arr) / sizeof(arr[0]);
    int search_num, result;

    printf("Enter a number to search: ");
    scanf("%d", &search_num);

    result = binarySearch(arr, 0, size - 1, search_num);

    if (result == -1) {
        printf("%d not found in the array\n", search_num);
    } else {
        printf("%d found at index %d\n", search_num, result);
    }

    return 0;
}
