##### Note: An array with one element is a sorted array

## Selection Sort
1. Divide the array in two parts viz. sorted and unsorted
2. In each round, select the smallest element from the
   unsorted part
3. Push the selected element at the end of the sorted array

### Example: 3 4 5 2 1
- 1 | 3 4 5 2
- 1 2 | 3 4 5
- 1 2 3 | 4 5
- 1 2 3 4 | 5

## Bubble Sort
1. In each round, swap adjacent elements, for n - 1 rounds
2. Every round, the greatest number will be sorted into its
   correct position

### Example: 3 4 5 2 1
- 3 4 2 1 | 5
- 3 2 1 | 4 5
- 2 1 | 3 4 5
- 1 | 2 3 4 5

## Insertion Sort
1. At the start, we assume that the first element is sorted
   and the rest are unsorted
2. We compare the second element to the first and swap them
   to their correct positions
3. We keep swapping the first unsorted element into the
   sorted part until it reaches its correct position

### Example: 3 4 5 2 1
- 3 4 | 5 2 1
- 3 4 5 | 2 1
- 2 3 4 5 | 1
- 1 2 3 4 5 |