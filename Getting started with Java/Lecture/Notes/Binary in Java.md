# How Binary Numbers are stored in Java

- The most significant digit is reserved for sign (`0` for plus and `1` for
minus)

- Therefore, the largest number that can be stored in a byte is `127`

## Negative Numbers

- For negative numbers, we take the 2's compliment of the positive number

- This automatically switches the first digit to `1` signifying negative

- To read a negative binary number, we take its 2's compliment

- `1000 0000` is a negative number who's 2's compliment is also the same

- Which is why the smallest number that can be stored in a byte is `-128`

**Note**: *A `32 bit` JVM will process 32 bits at a time and a `64 bit` JVM
will process 64 bits at a time. If given a smaller data type, it will prefix
zeroes before processing it.*
