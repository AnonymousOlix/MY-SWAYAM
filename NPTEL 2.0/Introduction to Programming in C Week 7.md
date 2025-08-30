# Introduction to Programming in C Week 7

# Week 7

# Programming Assignment 1

```bash
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

struct Student {
    char name[21];   // max 20 chars + null terminator
    int physics;
    int chemistry;
    int maths;
};

// comparator for qsort
int compare(const void *a, const void *b) {
    struct Student *s1 = (struct Student *)a;
    struct Student *s2 = (struct Student *)b;

    // Rule 1: Physics descending
    if (s1->physics != s2->physics) {
        return s2->physics - s1->physics;
    }

    // Rule 2: Chemistry descending
    if (s1->chemistry != s2->chemistry) {
        return s2->chemistry - s1->chemistry;
    }

    // Rule 3: Maths descending
    return s2->maths - s1->maths;
}

int main() {
    int n;
    scanf("%d", &n);

    struct Student arr[100];

    for (int i = 0; i < n; i++) {
        scanf("%s %d %d %d", arr[i].name, 
                             &arr[i].physics,
                             &arr[i].chemistry,
                             &arr[i].maths);
    }

    qsort(arr, n, sizeof(struct Student), compare);

    for (int i = 0; i < n; i++) {
        printf("%s %d %d %d\n", arr[i].name,
                                arr[i].physics,
                                arr[i].chemistry,
                                arr[i].maths);
    }

    return 0;
}

```

# Programming Assignment 2

```bash
#include <stdio.h>
#include <stdlib.h>

struct node {
    int id;
    int priority;
    struct node *next;
};

// Create and return a node with given id and val
struct node *create_node(int id, int val) {
    struct node *new_node = (struct node *)malloc(sizeof(struct node));
    new_node->id = id;
    new_node->priority = val;
    new_node->next = NULL;
    return new_node;
}

// Add node e at the beginning of list and return new head
struct node *append(struct node *list, struct node *e) {
    e->next = list;
    return e;
}

// Search for node with id and return pointer to it or NULL if not found
struct node *search(struct node *list, int id) {
    struct node *temp = list;
    while (temp != NULL) {
        if (temp->id == id) {
            return temp;
        }
        temp = temp->next;
    }
    return NULL;
}

// Change priority of node with id to val, do nothing if not found
void change_priority(struct node *list, int id, int val) {
    struct node *node_ptr = search(list, id);
    if (node_ptr != NULL) {
        node_ptr->priority = val;
    }
}

int main() {
    char op;
    int id, val;
    struct node *list = NULL;

    while (1) {
        scanf(" %c", &op);
        if (op == 'E') {
            break;
        } else if (op == 'A') {
            scanf("%d %d", &id, &val);
            struct node *new_node = create_node(id, val);
            list = append(list, new_node);
        } else if (op == 'C') {
            scanf("%d %d", &id, &val);
            change_priority(list, id, val);
        } else if (op == 'S') {
            scanf("%d", &id);
            struct node *found = search(list, id);
            if (found != NULL) {
                printf("%d %d\n", found->id, found->priority);
            } else {
                printf("%d -1\n", id);
            }
        }
    }

    // Free allocated memory (optional for this problem)
    struct node *temp;
    while (list != NULL) {
        temp = list;
        list = list->next;
        free(temp);
    }
    return 0;
}
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
