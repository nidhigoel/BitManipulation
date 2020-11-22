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

x & (x-1) will clear the lowest set bit of x

x & ~(x-1) extracts the lowest set bit of x (all others are clear). Pretty patterns when applied to a linear sequence.

x & (x + (1 << n)) = x, with the run of set bits (possibly length 0) starting at bit n cleared.

x & ~(x + (1 << n)) = the run of set bits (possibly length 0) in x, starting at bit n.

x | (x + 1) = x with the lowest cleared bit set.

x | ~(x + 1) = extracts the lowest cleared bit of x (all others are set).

x | (x - (1 << n)) = x, with the run of cleared bits (possibly length 0) starting at bit n set.

x | ~(x - (1 << n)) = the lowest run of cleared bits (possibly length 0) in x, starting at bit n are the only clear bits
