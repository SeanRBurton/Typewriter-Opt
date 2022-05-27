# Typewriter-Opt

Using dynamic programming to solve the problem posed by http://hardmath123.github.io/crown-typewriter.html#comment-toggle to optimality. Given the probability of transitioning between each pair of letters, what is the sequential layout which minimizes the expected transition distance (weighted by the corresponding probabilities)?

If we lay the letters out left to right, then you can think of adding a letter to the layout as doing two things:

1) Pushing the assigned letters away from the unassigned letters by a distance of 1.
2) Moving the new letter from the unassigned set to the assigned set.

We can compute the change in cost independent of the order of the assigned letters, so we can use dynamic programming over assigned subsets. This reduces the complexity from n! to 2^n, and makes it possible to prove the optimal solution in less than 30 seconds.
