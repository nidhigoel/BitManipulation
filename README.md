# BitManipulation

https://youtu.be/Etoggf42trE
https://www.youtube.com/watch?v=zxb8DvLUqcM

Quora questions :-

https://www.quora.com/What-is-an-intuitive-explanation-for-why-x-x-1-always-equals-x-with-the-lowest-bit-erased

Tactics :-

https://www.topcoder.com/community/competitive-programming/tutorials/a-bit-of-fun-fun-with-bits/

https://www.geeksforgeeks.org/bits-manipulation-important-tactics/

https://www.hackerearth.com/practice/notes/bit-manipulation/

Practice :-

clear the lowest set bit of x -> x & (x-1)

extract the lowest set bit of x, (all others are clear) -> x & ~(x-1)

set the lowest cleared bit of x -> x | (x + 1)

extracts the lowest cleared bit of x, (all others are set) -> x | ~(x + 1)

**Clear the run of set bit starting at bit n of x** 
x & (x + (1 << n))

1<<n will be all 0s with 1 at (n+1)th bit.
For eg 1<<2 = 100

x+(1 << n)
will give same bit as x for first n positions
clear the continous run of set bits in x from nth position
first non set bit after the continous run of set bits  will be set
rest of the bits remain same

x & (x + (1 << n))
will give same bit as x for first n positions
0 for the continous run of set bits in x from nth position
first non set bit after the continous run of set bits will be 0
rest of the bits remain same

Hence only the run of set bit starting at bit n of x are cleared, rest remain same

**the run of set bits starting at bit n of x**
x & ~(x + (1 << n))

set the run of cleared bit starting at bit n of x -> x | (x - (1 << n))

the lowest run of cleared bits (possibly length 0) in x, starting at bit n are the only clear bits -> x | ~(x - (1 << n))
