## Ex16 — Check for Balanced Parentheses Using Stack

## AIM:
To write a Java program that verifies whether the parentheses (brackets) in an input string are balanced — meaning each opening bracket has a corresponding and correctly ordered closing bracket.

## Algorithm

Create an empty stack.

Traverse each character in the string.

If an opening bracket appears, push it onto the stack.

If a closing bracket appears:

If the stack is empty → unbalanced

Else pop and verify the type of bracket

After processing all characters:

If stack is empty → Balanced

Else → Not Balanced

## Program
```
Program to verify whether the parentheses (brackets) in an input string are balanced
Developed by: Naresh P.S.
RegisterNumber: 212223040127
Date: 15-11-2025


import java.util.*;

public class BalancedParentheses {
    public static boolean isBalanced(String s) {
        Stack<Character> stack = new Stack<>();

        for (char ch : s.toCharArray()) {
            if (ch == '(' || ch == '{' || ch == '[') {
                stack.push(ch);
            } else if (ch == ')' || ch == '}' || ch == ']') {
                if (stack.isEmpty()) return false;

                char top = stack.pop();
                if ((ch == ')' && top != '(') ||
                    (ch == '}' && top != '{') ||
                    (ch == ']' && top != '[')) {
                    return false;
                }
            }
        }
        return stack.isEmpty();
    }

    public static void main(String[] args) {
        String input = "({[]})";
        System.out.println("Balanced: " + isBalanced(input));
    }
}
```
## Output
Balanced: true

## Result

Thus, the program correctly checks whether an input string has balanced parentheses using a stack.
