The Purpose of this assignment is to create an algorithm that efficiently calculates the maximum cycle length over a range of numbers when the Collatz conjecture is applied.

The Collatz Conjecture states that when you follow these steps:

If a number is even, divide the number by two.
If a number is odd, multiple the number by three and add one.

You will end up at the number one.

This can be seen the following examples:

1
2 -> 1
3 -> 10 -> 5 -> 16 -> 8 -> 4 -> 2 -> 1

The cycle lengths for the above sequences are respectively 1 , 2, 8

The Naive algorithm written follows these steps explicitly.

The first optimization implemented took advantage of the fact that the process for an odd number will certainly produce an even which then can be immediately reduced in half. By also applying a bitwise operation in order to increase efficiency you then can use " i + (i >>1) +1" and increment by two where i is the next odd number in the sequence of cycle length calculation.

The Next optimization quickly checks to see if the beginning of the range is less than half of the top of the range. If so, then the beginning of the range can be altered to be half of the top of the range. This is due to the fact that any number that is below the half-way point can map itself to a number in the upper half of the range by multiplying itself by an even integer. This means that no number in the lower part of the range can possess the maximum cycle length for the entire range.

The last optimization implements a lazy cache, that as the program runs, adds the numbers it has calculated the cycle length for to a local array with a capacity of a million. This way, time is saved by not having to calculate each number every time it is seen.