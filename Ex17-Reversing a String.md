## Ex17 — Reverse a String Using Stack

## AIM:
To write a Java program that reverses an input string using a stack, without using built-in reverse functions.

## Algorithm

Create an empty stack.

Push each character of the string onto the stack.

Pop characters from the stack to form the reversed string.

Display the reversed output.

## Program
```
Program to reverse an input string using a stack
Developed by: Naresh P.S.
RegisterNumber: 212223040127
Date: 15-11-2025

import java.util.*;

public class ReverseStringStack {
    public static void main(String[] args) {
        String str = "Naresh";
        Stack<Character> stack = new Stack<>();

        for (char c : str.toCharArray()) {
            stack.push(c);
        }

        String reversed = "";
        while (!stack.isEmpty()) {
            reversed += stack.pop();
        }

        System.out.println("Reversed String: " + reversed);
    }
}
```

## Output
Reversed String: hseraN

## Result

Thus, the program successfully reverses the given string using a stack without relying on built-in reverse functions.
