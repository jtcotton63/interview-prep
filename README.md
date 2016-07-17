# CS Basics
Covers basic computer science ideas in brief

## Searches
### Binary Search
Divides the search space in half each time.

**Prerequsites:**
 * Array is the backing data structure
 * The array must be sorted

Pretend that the target value is 13.

Start by defining three points called start, middle, and end:
![](https://github.com/jtcotton63/cs-basics/blob/master/images/searches/binary/define-pointers.png)

Evaluate the value at ````array[middle]````

There are three cases that can happen:
 * ````array[mid] == x```` (where x is the item we're looking for)
   * You've found the item you're looking for. Return.
 * ````array[mid] > x````
   * Set ````end = mid - 1````
   * Reevaluate midpoint ````((start + end) / 2)````
   * Recurse
 * ````array[mid] < x````
   * Set ````start = mid + 1````
   * Reevaluate midpoint ````((start + end) / 2)````
   * Recurse
 
Recursing once resets the pointers and reduces the search space by half the number of elements:
![](https://github.com/jtcotton63/cs-basics/blob/master/images/searches/binary/resetting-pointers.png)

 **Runtime:** O(log(n))
