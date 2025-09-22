# Lab 04 - SOP/POS and KMaps

In this lab, you’ve learned how to apply KMaps, Sum Of Products and Products of
sums to simplify digital logic equations. Then, you’ve proven out that they work
using an implemented design on your Basys3 boards.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Summary

In this lab we learned how to use K-Maps to make logic equations simpler. We first started with the truth table, wrote the full equations, and then reduced them into sum of products and product of sums. We also tested the dessigns on the Basys3 board and also checked them with simulation to make sure the outputs actually matched.

## Lab Questions

### Why are the groups of 1’s (or 0’s) that we select in the KMap able to go across edges?
They're able to go across because the K-Map actually wraps around. The left and right edges, and top and bottom are basically neighboring each other. This works since only one variable changes between edges.

### Why are the names Sum of Products and Products of Sums?
With SOP you take all the product terms and add them up with OR gates, but with POS you take all the sum terms and multiply them together with AND gates.

### Open the test.v file – how are we able to check that the signals match using XOR?
The XOR outputs 0 if the two signals are the same. In the test file, if led[0] ^ led[1] is not 0 ten that really just means they don't match. That way we know all three versions (naive, minterm, maxterm) are producing the exact same result.
