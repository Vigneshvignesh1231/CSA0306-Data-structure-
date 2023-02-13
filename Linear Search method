#include <stdio.h>

int main() {
    int arr[] = {1, 4, 6, 8, 9, 11, 14, 15, 20, 25};
    int size = sizeof(arr) / sizeof(arr[0]);
    int search_num, i, flag = 0;

    printf("Enter a number to search: ");
    scanf("%d", &search_num);

    for (i = 0; i < size; i++) {
        if (arr[i] == search_num) {
            printf("%d found at index %d\n", search_num, i);
            flag = 1;
            break;
        }
    }

    if (flag == 0) {
        printf("%d not found in the array\n", search_num);
    }

    return 0;
}
