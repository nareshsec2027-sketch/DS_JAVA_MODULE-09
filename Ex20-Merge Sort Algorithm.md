## Ex20 — Sorting an Array Using Merge Sort

## AIM:
To design a program that sorts a given array of integers in ascending order using the Merge Sort algorithm without built-in sorting functions.

## Algorithm

Divide the array into two halves.

Recursively sort each half.

Merge both sorted halves.

Display the final sorted array.

## Program
```
Program to sort a given array using Merge Sort
Developed by: Naresh P.S.
RegisterNumber: 212223040127
Date: 15-11-2025


public class MergeSortProgram {

    void merge(int arr[], int l, int m, int r) {
        int n1 = m - l + 1;
        int n2 = r - m;

        int L[] = new int[n1];
        int R[] = new int[n2];

        for (int i = 0; i < n1; ++i) L[i] = arr[l + i];
        for (int j = 0; j < n2; ++j) R[j] = arr[m + 1 + j];

        int i = 0, j = 0, k = l;

        while (i < n1 && j < n2) {
            if (L[i] <= R[j]) arr[k++] = L[i++];
            else arr[k++] = R[j++];
        }

        while (i < n1) arr[k++] = L[i++];
        while (j < n2) arr[k++] = R[j++];
    }

    void sort(int arr[], int l, int r) {
        if (l < r) {
            int m = (l + r) / 2;
            sort(arr, l, m);
            sort(arr, m + 1, r);
            merge(arr, l, m, r);
        }
    }

    public static void main(String args[]) {
        int arr[] = {12, 11, 13, 5, 6, 7};

        MergeSortProgram obj = new MergeSortProgram();
        obj.sort(arr, 0, arr.length - 1);

        System.out.print("Sorted array: ");
        for (int a : arr) System.out.print(a + " ");
    }
}
```

## Output
Sorted array: 5 6 7 11 12 13

## Result

The program sorts the given array using the Merge Sort algorithm with O(n log n) time complexity and minimal extra space.
