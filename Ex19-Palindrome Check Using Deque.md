## Ex19 — Palindrome Check Using Deque

## AIM:
To design a program that checks whether a given message is a palindrome using a deque after removing non-alphanumeric characters and converting to lowercase.

## Algorithm

Remove all non-alphanumeric characters.

Convert text to lowercase.

Insert characters into a deque.

Compare front and rear characters until deque is empty.

If all match → palindrome, else not.

## Program
```
Program to check whether a message is a palindrome using Deque
Developed by: Naresh P.S.
RegisterNumber: 212223040127
Date: 15-11-2025

import java.util.*;

public class PalindromeDeque {
    public static boolean isPalindrome(String s) {
        s = s.replaceAll("[^a-zA-Z0-9]", "").toLowerCase();

        Deque<Character> deque = new LinkedList<>();
        for (char c : s.toCharArray()) deque.add(c);

        while (deque.size() > 1) {
            if (deque.removeFirst() != deque.removeLast()) return false;
        }
        return true;
    }

    public static void main(String[] args) {
        String msg = "A man, a plan, a canal: Panama";
        System.out.println("Is Palindrome: " + isPalindrome(msg));
    }
}
```

Output
Is Palindrome: true

Result

The program successfully processes the string and determines whether it is a palindrome using a deque.
