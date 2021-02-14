# Large Arithmetic Collider FAQ

**What does the test output mean?**

Most tests are property-based and will show the randomly generated input for your function in pink/purple (usually - your terminal colours may affect this). Errors or incorrect outputs are shown in red and expected outputs in green (if applicable). Unit tests have different output, but explain that output. If you don't see the pink/purple values, make sure you are not using Powershell in which case the background colour of the terminal is the same as that of the output.

**My code passes the 4th test for `solve`, but none of the first three. Does this mean my code is correct?**

No, the fourth test for `solve` just tests that your `solve` function returns _something_ for every grid in the simple grids campaign. It does not validate that those results are correct. The other three tests check that results returned by your `solve` function are correct. In general, you need to pass all tests for a given function or there is guaranteed to be something wrong with your implementation. 

**What should `steps` return if there is no solution?**

The `steps` function should return the empty list if there is no solution.

**May I assume an upper limit for the number of rotations that will be required in `steps`?**

No, your function should work regardless of the number of rotations that may be required to find a solution. If there is a solution, it should theoretically always find it and if there is no solution, it should eventually discover this.

**The tests for `steps` fail, but I don't know why.**

Make sure that you do _not_ include the starting grid in the resulting sequence and make sure that the last grid in the sequence is the last move as a solution.

**What should I do if there are multiple sequences for `steps` that lead to a solution in the minimum number of moves or what if the grid that is found has multiple solutions in `steps`?**

Just return the first, shortest sequence you find. If there are multiple solutions for the grid you find with `steps`, just use the first solution returned by `solve` for it.
