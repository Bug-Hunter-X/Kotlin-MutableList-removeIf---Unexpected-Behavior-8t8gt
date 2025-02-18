# Kotlin MutableList removeIf() Unexpected Behavior
This repository demonstrates a subtle bug in Kotlin related to modifying a MutableList while iterating over it using the removeIf() function.

## Bug Description
The `removeIf()` function in Kotlin modifies the list in-place.  When using this function while iterating or processing the list using another method (such as a loop), unexpected behavior can result because the list's size and element positions are changing during the iteration.

## How to Reproduce
1. Clone this repository.
2. Run the `bug.kt` file. 
3. Observe that the output is different than expected. The expected output would be removing even numbers.
4. Run the `bugSolution.kt` file. Observe the correct output.

## Solution
The solution involves using an iterator to safely remove elements while iterating.