# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
```
1. Start the program.
2.Read an integer n → size of the array.
3.Create an integer array arr of size n.
4.Read all n elements and store them in the array.
5.Recursive Function
6.End the Program.
```   

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: Yuvaram S
RegisterNumber: 212224230315
*/

import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n)
    {
        
       if (i == n - 1) {
            return arr[i];
        }
        int minRest = getMin(arr, i + 1, n);
        return Math.min(arr[i], minRest);
        
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}

```

## Output:

<img width="492" height="374" alt="image" src="https://github.com/user-attachments/assets/eae1eb65-6412-4f34-9baf-b2ec7d3ea276" />

## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
