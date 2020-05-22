#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) For this answer I want to say that the runtime looks like quadratic time, but intuitively I feel it is not the case.  Instead I would say the runtime is O(n) due to the relationship between n^3, and n^2; which is simply n.


b) Runtime for b is logarithmic because for the value n, the loop will simply perform a single operation for all of the elements, and stagnating at the end.


c) The runtime for this should also be O(n) because it is simply calling itself recursively.

## Exercise II
For this problem, I would want to approach it using binary search.  It would allow for the one to eliminate large sections of floors instantly.  For instance, if we have f floors, if we use BST for for every time the egg is dropped we either have broken egg or not broken egg.  Best case scenario, is f has 2 floors, egg would need to be dropped a minimum of 1 time if it breaks from floor 1, a minimum of 2 times if it breaks from floor 2.  So this would necessitate that the we incorporate the number of eggs == the number of f for edge cases.  Because if the number of eggs == the number of floors, we can simply drop from the drop as well, and do a BST of sorts, that would begin with edge cases first, then expand from the root node.  Interesting question, but I would have to say it is something like:

`
def egg_counts(floors, eggs):
    if egg_drop(floors[-1]) == break:
        if egg_drop(floors[:]//2) == break:
            egg_counts(floors[:]//2, eggs)
        else:
            return egg_drops + egg_counts(floors, eggs)    
    return egg_drops += 1 + egg_counts(floors, eggs)        

`
