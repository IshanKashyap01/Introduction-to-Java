## Left shift <<
Shifts LHS to the left by RHS bits while keeping
the size same.

10 << 1 = 0000 1010 << 1 = 0001 0100 = 20

Generally it equals LHS multiplied by 2 raised by
RHS unless there's a sign change after shifting.

64 << 1 = 0100 0000 << 1 = 1000 0000 = -128

## Right shift >>
Shifts LHS to the right by RHS bits while keeping
the size same, while keeping the sign bit same.

10 >> 1 = 0000 1010 = 0000 0101 = 5

Equals LHS divided by 2 raised by RHS

-128 >> 1 = 1000 0000 >> 1 = 1100 0000 = -64