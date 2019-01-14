# Sorts
## Bubble sort
[Bubble sort video](https://www.youtube.com/watch?v=P00xJgWzz2c)

Psuedocode:
````
for i = (n - 1) to 1
	for j = 0 to (i - 1)
		if array[j] > array[j + 1]
			swap(array[j], array[j + 1]);

````

## Heap sort
Add all the elements to a sorted heap implementation. The heap should resort the heap every time a new element is inserted.
[Heap implementation video](https://www.youtube.com/watch?v=v1YUApMYXO4)
[Heap sort video](https://www.youtube.com/watch?v=6NB0GHY11Iw)

## Insertion sort
Psuedocode:
 * Insert element into array
 * If it has a smaller value than the one at the index previous to it, swap them. Repeat until the previous element has a smaller value than the current element
 
[Insertion sort video](https://www.youtube.com/watch?v=c4BRHC7kTaQ)

## Merge sort
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