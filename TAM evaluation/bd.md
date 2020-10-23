## b

In every recursive method optimalLossRecursive, there are 4 choice: 1. start a full service 2. start a regular service 3. start a minor service 4. do nothing , and no matter what choice you make, the currentHour is increasing all the time. So the worst case we got is a Quadtree  whose maximum depth is k, and the recursive method itself only need to compute a rangesum which is $O(4)$ and can be reduced to $O(1)$ by presum. 

So the lower bound on the worst-case time complexity of the recursive algorithm from Q1(a) is $O(4^k)$.

## d

First assume the length of fullServiceCapacity is n, length of regularServiceCapacity  is m, length of minorServiceCapacity is p. 

Our state dp(i,j) reprsents the minumLoss before start a service j at time i . Evert dp state will jump to next state in terms of how long the service last. For example a fullservice start point will jump to n*3 other state.

So the upper bound on the worst-case time complexity of your dynamic programming solution for part (c) , which is $O(3*k*max(n,m,p))$

