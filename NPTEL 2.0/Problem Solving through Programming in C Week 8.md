# Problem Solving through Programming in C

# Week 8

# Programming Assignment 1

```bash
#include <stdio.h>
#include <stdlib.h>

struct ListNode {
    int val;
    struct ListNode* next;
};

// create new node
struct ListNode* newNode(int val) {
    struct ListNode* node = (struct ListNode*)malloc(sizeof(struct ListNode));
    node -> val = val;
    node -> next = NULL;
    return node;
}

// add two numbers represented by linked lists
struct ListNode* addTwoNumbers(struct ListNode* l1, struct ListNode* l2) {
    struct ListNode* dummy = newNode(0);
    struct ListNode* curr = dummy;
    int carry = 0;

    while (l1 != NULL || l2 != NULL || carry != 0) {
        int x = (l1 != NULL) ? l1 -> val : 0;
        int y = (l2 != NULL) ? l2 -> val : 0;

        int sum99 = x + y + carry;
        carry = sum99 / 10;

        curr -> next = newNode(sum99 % 10);
        curr = curr -> next;

        if (l1 != NULL) l1 = l1 -> next;
        if (l2 != NULL) l2 = l2 -> next;
    }

    return dummy->next; // skip dummy head
}

// append node at end
void appendNode(struct ListNode** head, int val) {
    struct ListNode* node = newNode(val);
    if (*head == NULL) {
        *head = node;
        return;
    }
    struct ListNode* temp = *head; 
    while (temp -> next != NULL) temp = temp -> next;
    temp -> next = node;
}

// print linked list
void printList(struct ListNode* head) {
    while (head != NULL) {
        printf("%d", head -> val);
        if (head -> next != NULL) printf(" ");
        head = head -> next;
    }
}

// read a linked list from one line of input
struct ListNode* readList() {
    struct ListNode* head = NULL;
    int x;
    while (scanf("%d", &x) == 1) {
        appendNode(&head, x);
        int c = getchar();
        if (c == '\n' || c == EOF) break;
    }
    return head;
}

int main() {
    struct ListNode* l1 = readList();
    struct ListNode* l2 = readList();

    struct ListNode* result = addTwoNumbers(l1, l2);
    printList(result);

    return 0;
}
```

# Programming Assignment 2

```bash
#include <stdio.h>
#include <stdlib.h>

struct ListNode {
    int val;
    struct ListNode* next;
};

// function to merge two sorted linked lists
struct ListNode* mergeTwoLists(struct ListNode* l1, struct ListNode* l2) {
    struct ListNode dummy;  // dummy head
    struct ListNode* tail = &dummy;
    dummy.next = NULL;

    while (l1 != NULL && l2 != NULL) {
        if (l1 -> val <= l2 -> val) {
            tail -> next = l1;
            l1 = l1 -> next;
        } else {
            tail -> next = l2;
            l2 = l2 -> next;
        }
        tail = tail -> next;
    }

    // append remaining nodes
    if (l1 != NULL) tail -> next = l1;
    if (l2 != NULL) tail -> next = l2;

    return dummy.next;  // return merged list head
}

// create new node
struct ListNode* newNode(int val) {
    struct ListNode* node = (struct ListNode*)malloc(sizeof(struct ListNode));
    node -> val = val;
    node -> next = NULL;
    return node;
}

// append node to linked list
void appendNode(struct ListNode** head, int val) {
    struct ListNode* node = newNode(val);
    if (*head == NULL) {
        *head = node;
        return;
    }
    struct ListNode* temp = *head;
    while (temp->next != NULL) temp = temp -> next;
    temp -> next = node;
}

// print linked list
void printList(struct ListNode* head) {
    while (head != NULL) {
        printf("%d", head -> val);
        if (head -> next != NULL) printf(" ");
        head = head->next;
    }
}

struct ListNode* readList() {
    struct ListNode* head = NULL;
    int x;
    char ch85;

    while (scanf("%d", &x) == 1) {
        appendNode(&head, x);
        ch85 = getchar();
        if (ch85 == '\n' || ch85 == EOF) break;
    }

    return head;
}

int main() {
    struct ListNode* l1 = readList();
    struct ListNode* l2 = readList();

    struct ListNode* merged = mergeTwoLists(l1, l2);

    printList(merged);

    return 0;
}
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
