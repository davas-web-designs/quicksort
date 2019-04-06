# Quicksort alogrithm
## Features:
1. Divide an conquer strategy
2. (Average) Time complexity: O(nlogn)
3. Recursive algorithm

Explication:
  arr = [7, 2, 6, 5, 4] pivot = 4
  -> [2,4,7,6,5] index = 1
  -> [2,4,7,6,5] pivot = 5
    -> [5,7,6]
      -> [6,7]
  The array is going to be subdiveded recursively
  Take a pivot, (in this particular example it is the number 4 at the end of the array) and put every value that is less than that pivot to one side and every greater value to the other side

funcion quicksort(arr, start, end){
  stop when start >= end

  let index = partition(arr, start, end, pivot)
  //the index value of where the pivot ended up

  //divide and conquer:
  quicksort(arr, start, index-1)
  quicksort(arr, index + 1, end)

}

function partition(arr, start, end){
  arr = [9, 3, 4, 6, 5]
  pivot = 5  
  index = 0
  i = 0, i -> end-1
    if arr[i] < pivot?
      swap i, index
      index++
  swap pivot, end
}

calling partition:
  partition(arr, 0, 4)
