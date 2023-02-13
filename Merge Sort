#include <stdio.h>
void merge(int arr[], int left[], int leftCount, int right[], int rightCount) {
    int i = 0, j = 0, k = 0;
    while (i < leftCount && j < rightCount) {
        if (left[i] < right[j])
            arr[k++] = left[i++];
        else
            arr[k++] = right[j++];
    }
    while (i < leftCount)
        arr[k++] = left[i++];
    while (j < rightCount)
        arr[k++] = right[j++];
}
void mergeSort(int arr[], int n) {
    int i;
	if (n < 2)
        return;
    int mid = n / 2;
    int left[mid];
    int right[n - mid];
    for (i = 0; i < mid; i++)
        left[i] = arr[i];
    for (i = mid; i < n; i++)
        right[i - mid] = arr[i];
    mergeSort(left, mid);
    mergeSort(right, n - mid);
    merge(arr, left, mid, right, n - mid);
}

int main() {
    int arr[] = {38, 27, 43, 3, 9, 82, 10},i;
    int n = sizeof(arr) / sizeof(arr[0]);
    mergeSort(arr, n);
    printf("Sorted array: \n");
    for (i = 0; i < n; i++)
        printf("%d ", arr[i]);
    return 0;
}
