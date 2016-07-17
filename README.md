# CS Basics
Covers basic computer science ideas in brief

## Searches
### Binary Search
Divides the search space in half each time.

**Prerequsites:**
 * Array is the backing data structure
 * The array must be sorted

Start by defining three points called start, middle, and end.

Evaluate the value at ````array[middle]````

There are three cases that can happen:
 * ````array[mid] == x```` (where x is the item we're looking for)
   * You've found the item you're looking for. Return.
 * ````array[mid] > x````
   * Set ````end = mid - 1```` and recurse.
 * ````array[mid] < x````
   * Set ````start = mid + 1```` and recurse.
 
 **Runtime:** O(log(n))
