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
 
### Linear Search
Linear search is iterating over every element in the data structure one by one until the desired value is found.

An example:
````
  array[5] = {0,2,4,6,8}
  int searchTerm = 6;
  for(int i = 0; i < array.length; i++)
    if(array[i] == searchTerm)
      return i;
      
  return -1;  // searchTerm not found
````

## Sorts
### Bubble sort
[Bubble sort video](https://www.youtube.com/watch?v=P00xJgWzz2c)

Psuedocode:
````
for i = (n - 1) to 1
	for j = 0 to (i - 1)
		if array[j] > array[j + 1]
			swap(array[j], array[j + 1]);

````

### Heap sort
Add all the elements to a sorted heap implementation. The heap should resort the heap every time a new element is inserted.
[Heap implementation video](https://www.youtube.com/watch?v=v1YUApMYXO4)
[Heap sort video](https://www.youtube.com/watch?v=6NB0GHY11Iw)

### Insertion sort
Psuedocode:
 * Insert element into array
 * If it has a smaller value than the one at the index previous to it, swap them. Repeat until the previous element has a smaller value than the current element
 
[Insertion sort video](https://www.youtube.com/watch?v=c4BRHC7kTaQ)

### Merge sort
Merge sort takes two sorted arrays and merges them into a larger array.

Psuedocode:
````
// First do something like this
private void doMergeSort(int lowerIndex, int higherIndex) {
     
    if (lowerIndex < higherIndex) {
        int middle = lowerIndex + (higherIndex - lowerIndex) / 2;
        // Below step sorts the left side of the array
        doMergeSort(lowerIndex, middle);
        // Below step sorts the right side of the array
        doMergeSort(middle + 1, higherIndex);
        // Now merge both sides
        mergeParts(lowerIndex, middle, higherIndex);
    }
}

// Then do something like this
public void merge(int[] A, int[] B) {

	int[] C = new int[A.length + B.length];

	int aIndex = 0;
	int bIndex = 0;
	int cIndex = 0;

	while(cIndex < C.length) {

		int currMinValue = 0;

		if(aIndex < A.length && A[aIndex] < B[bIndex]]) {
			currMinValue = A[aIndex];
			aIndex++;
		} else {
			currMinValue = B[bIndex];
			bIndex++;
		}

		C[cIndex] = currMinValue;
		cIndex++;

	}

}
````
[Merge sort video](https://www.youtube.com/watch?v=GCae1WNvnZM)

## Trees
### Binary Search Tree
A binary tree (each node has only two branches) in which the left subtree is always lesser and the right subtree is always greater than the value of the current node. (Duplicates vary according to the implementation).

![](https://github.com/jtcotton63/cs-basics/blob/master/images/trees/binary-search/example.png)

**Search time:** O(log(n))

**Insertion time:** O(log(n))

**Deletion time:** O(log(n))
 
 
