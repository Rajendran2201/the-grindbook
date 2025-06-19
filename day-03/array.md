# Arrays

- Array as a data structure 
- deep copy and shallow copy 
- Reversing an array


- Insertion or deletion in an array is a expensive process. 

let's try inserting an element into an array 

```java
public class ArrayOperations{

  public static int[] insert(int[] arr, int index, int num){
    int[] res = new int[arr.length + 1];
    int pointer = 0;
    for(int i=0; i<res.length; i++){
      if(i == index){
        res[i] = num;
      }else{
          res[i] = arr[pointer++];
      }
    }
    return res;
  }
  public static int[] remove(int[] arr, int index){
    int[] res = new int[arr.length - 1];
    int pointer = 0;
    for(int i=0; i<res.length; i++){
      if(pointer == index){
       pointer++;
      }
      res[i] = arr[pointer++];
    }
    return res;
  }
  public static void printArray(int[] arr){
    for(int num: arr){
      System.out.print(" " + num);
    }
  }

  public static void main(String args[]){
    int[] arr = {1,4,5,2,6};
    System.out.print("\nBefore Insertion: ");
    printArray(arr);

    arr = insert(arr, 2, 9);
    System.out.print("\nAfter Insertion: ");
    printArray(arr);

    arr = remove(arr, 3);
    System.out.print("\nAfter Removal: ");
    printArray(arr);
  }
}
```

**Sample output:**

```bash
Before Insertion:  1 4 5 2 6
After Insertion:  1 4 9 5 2 6
After Removal:  1 4 9 2 6
```