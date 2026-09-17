# Ex2 Count how many times a number appears in an array recursively.
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1. Start the program.
2. Read the size of the array size.
3. If size <= 0, print "Invalid array size" and stop the program.
4. Create an integer array arr of size size.
5. Read all the size elements and store them in the array arr.
6. Read the target number whose occurrences need to be counted.
7. If n == 0, return 0
8. Check the last element of the current array segment.
9. Store the returned value (count of occurrences) in the variable count.
10. Print the required.
11. End the program.  

## Program:
```
/*
Program Count how many times a number appears in an array recursively.
Developed by: Yuvaram S
RegisterNumber: 212224230315
*/

import java.util.Scanner;

public class CountOccurrences {
    public static int countOccurrences(int[] arr, int n, int target) {
        if (n == 0) {
            return 0; // Base case: no elements left
        }
        if (arr[n - 1] == target) {
            return 1 + countOccurrences(arr, n - 1, target);
        } else {
            return countOccurrences(arr, n - 1, target);
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int size = scanner.nextInt();

        if (size <= 0) {
            System.out.println("Invalid array size. Must be positive.");
            return;
        }
        int[] arr = new int[size];
        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }
        int target = scanner.nextInt();
        int count = countOccurrences(arr, size, target);
        System.out.println("The number " + target + " appears " + count + " time(s) in the array.");

        scanner.close();
    }
}

```

## Output:

<img width="1307" height="721" alt="image" src="https://github.com/user-attachments/assets/ca0d92ac-e504-4e1d-9790-6b13ca850116" />


## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
