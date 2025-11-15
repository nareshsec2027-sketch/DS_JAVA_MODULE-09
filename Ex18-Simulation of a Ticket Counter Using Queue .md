## Ex18 — Ticket Counter Simulation Using Queue (Linked List)

## AIM:
To simulate the functioning of a ticket counter that operates on FIFO order using a queue implemented via a linked list.

## Algorithm

Create a Queue using LinkedList.

Enqueue customers as they arrive.

Dequeue customers as they are served.

Display the queue at each step.

## Program
```
Program to simulate the functioning of a ticket counter using FIFO queue
Developed by: Naresh P.S.
RegisterNumber: 212223040127
Date: 15-11-2025


import java.util.*;

public class TicketCounter {
    public static void main(String[] args) {
        Queue<String> queue = new LinkedList<>();

        queue.add("Customer 1");
        queue.add("Customer 2");
        queue.add("Customer 3");

        System.out.println("Queue: " + queue);

        System.out.println("Serving: " + queue.remove());
        System.out.println("Serving: " + queue.remove());

        System.out.println("Remaining Queue: " + queue);
    }
}
```

## Output
Queue: [Customer 1, Customer 2, Customer 3]
Serving: Customer 1
Serving: Customer 2
Remaining Queue: [Customer 3]

## Result

Thus, the program successfully simulates a ticket counter queue where customers are served in FIFO order using a linked list–based queue.
