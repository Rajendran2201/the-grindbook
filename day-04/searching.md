# Searching 

The searching in an array is of two types:
1. Linear Search - Unsorted array
2. Binary Search - Sorted array 

### Linear search 

```java
public class LinearSearch{
  public static int findIndex(int[] arr, int target){
    for(int i=0; i<arr.length; i++){
      if(arr[i] == target){
          return i;
      }
    }
    return -1;
  }
  public static void main(String args[]){
    int[] arr = {1,2,4,2,5,2,5};
    int target = 4;
    int pos = findIndex(arr, target);
    if(pos == -1){
        System.out.print("Element not found!"); return;
    }
    System.out.print("The element:" + target +" is found at the index:"+pos);
  }
}
```

### Binary Search 

>NOTE: Binary Search must be performed on a sorted array.

```java
public class BinarySearch{
    public static int findIndex(int[] arr, int target){
        int start = 0, end = arr.length - 1;
        while(start <= end){
            int mid = start + (end-start)/2;
            if(arr[mid] > target){
                end = mid - 1;
            }else if(arr[mid] < target){
                start = mid + 1;
            }else{
                return mid;
            }
        }
        return -1;
    }
    public static void main(String args[]){
    int[] arr = {1,2,4,5};
    int target = 4;
    int pos = findIndex(arr, target);
    if(pos == -1){
        System.out.print("Element not found!"); return;
    }
    System.out.print("The element:" + target +" is found at the index:"+pos);
  }
}
```