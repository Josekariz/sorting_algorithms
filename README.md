# 0x1B. C - Sorting algorithms & Big O

## Description

This project is meant to be completed by a team of two students. The goal of this project is to implement various sorting algorithms in C and understand their time complexities using Big O notation.

## Learning Objectives

By the end of this project, you should be able to:

- Implement at least four different sorting algorithms.
- Explain what Big O notation is and evaluate the time complexity of an algorithm.
- Select the best sorting algorithm for a given input.
- Understand what a stable sorting algorithm is.

## Requirements

- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89.
- All your files should end with a new line.
- A README.md file, at the root of the folder of the project, is mandatory.
- Your code should use the Betty style, and it will be checked using betty-style.pl and betty-doc.pl.
- You are not allowed to use global variables.
- No more than 5 functions per file.
- Unless specified otherwise, you are not allowed to use the standard library. Any use of functions like printf, puts, … is totally forbidden.
- The prototypes of all your functions should be included in your header file called `sort.h`.
- Don’t forget to push your header file.
- All your header files should be include guarded.

## Data Structures and Functions

For this project, you are given the following print_array and print_list functions:

```c
#include <stdlib.h>
#include <stdio.h>

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array && i < size)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}

#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i > 0)
            printf(", ");
        printf("%d", list->n);
        ++i;
        list = list->next;
    }
    printf("\n");
}
```

Our files `print_array.c` and `print_list.c` (containing the `print_array` and `print_list` functions) will be compiled with your functions during the correction. Please declare the prototype of the functions `print_array` and `print_list` in your `sort.h` header file.

Please use the following data structure for doubly linked list:

```c
/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;
```

## Time Complexity Notations (Big O)

You need to provide the time complexity notations of each sorting algorithm in a file named `0-O`, `1-O`, `2-O`, and `3-O`. Each file should contain three lines, one for each of the following cases:

1. Best case time complexity.
2. Average case time complexity.
3. Worst case time complexity.

Use the short notation (without constants) for Big O notation. For example, use `O(n)` instead of `O(2n)` or `O(nk)`.

## Tasks

### 0. Bubble sort

Write a function that sorts an array of integers in ascending order using the Bubble sort algorithm.

**Prototype:**

```c
void bubble_sort(int *array, size_t size);
```

### 1. Insertion sort

Write a function that sorts a doubly linked list of integers in ascending order using the Insertion sort algorithm.

**Prototype:**

```c
void insertion_sort_list(listint_t **list);
```

### 2. Selection sort

Write a function that sorts an array of integers in ascending order using the Selection sort algorithm.

**Prototype:**

```c
void selection_sort(int *array, size_t size);
```

### 3. Quick sort

Write a function that sorts an array of integers in ascending order using the Quick sort algorithm. Implement the Lomuto partition scheme, and always select the last element as the pivot.

**Prototype:**

```c
void quick_sort(int *array, size_t size);
```



## Author

- Team Member: Joseph Macharia

