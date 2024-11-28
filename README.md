# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

Asymptotic analysis may be misleading with respect to actual performance in practice because of using upper and lower bounds to make algorithms look better than they are, $n_0$ can be larger than needed, and it can be misrepresented.

1. The compexities of $O$ and $\Omega$ are upper and lower bounds for an algorithm. 
For an algorithm there is an $O(n)$ complexity associated to it, but we are able to find bounds that follow the algorithm more closely.
These closer complexitys would be a better for estimating the real performance then using the general complexities.

2. Asymptotic analysis by definition tells us that all $n \geq n_0$.
Since we are able to pick whichever $n_0$ we want that works within the bounds, we can pick overly large values.
Picking large values when they're not needed leaves room for error estimating real practice.

3. Asymptotic analysis by definition tells us that we're able to find a $f(n)$ that satisfies $T(n)$ ($\leq$ or $\geq$ or both) $Cf(n)$.
$C$ in any given analysis is unknown so smaller values such as $2f(n)$ is different than $50f(n)$.
This can misrepresent the total runtime of $T(n)$ in practice.

If given a binary search tree with 1,000 elements it takes 5 seconds to find a particular element, with what we know about asymptotic complexity, finding the same element in a search tree with 10,000 elements would take around 7 seconds.

Binary search tree complexity = $0(log_2(n))$

Binary search tree complexity of 1000 elements = $0(log_2(1000)) = 9.966$

Binary search tree complexity of 10000 elements = $0(log_2(10000)) = 13.288$

Using division you would find that 5/9.966 = x/13.288 => 66.439 = 9.966x => 6.666 = x. Using this logic you would find it would take around 7 seconds to find the same element in a binary tree of 10000 elements.

If you measure the time with 10,000 elements and it takes 100 seconds this could be the case given that reasonning with asymptotic complexity suggest a different time because of memory leaks, being ran on different machines, and oversized elements.

1. The algorithm could have a memory leak we don't know about.
If this is left unchecked we would have memory allocated for no reason to the point where it uses up all of our ram, and starts to use the hard drive for memory to run the algorithm which would cause a large hit to performance and runtime.
If you have to use your hard drive for memory it would increase runtime.

3. Running algorithms on different machines can yield different results, so this could've been ran on a different machine.
Different computers have different computing power, if you did the first test using a lab computer, then the second using a laptop at home, you could get different results.
Using a machine with less computing power could increase runtime.

4. The elements being to large.
If the elements weren't just numbers or strings, but large data such as video clips.
This would take much more time to analyize than just numbers or strings which would increase overall runtime.
