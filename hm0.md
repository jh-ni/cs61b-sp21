## Exercise 1a  \ 1b

```java
 public class Zeno {
    public static void main(String[] args) {
        int row = 1;
        int SIZE = 5;
        while (row <= SIZE) {
          int col = 0;
           while (col < row) { 
              System.out.print('*');
              col = col + 1;             
           }
            System.out.println();
            row = row + 1; 
        }    
    }
}

        }    
    }
}
```

```java
public class TriangleDrawer {
   public static void drawTriangle(int N) {
      int row = 1;
      int size = N;
      while (row <= size){
         int col = 0;
         while (col < row){
            System.out.print('*');
            col = col + 1;
         }
         row = row + 1;
         System.out.println();
      }
   }
   public static void main(String[] args) {
      drawTriangle(10);   /** 竟然是这样，void不可以输出，所以不用print直接调用就行 */
   }
}
```

## Exercise 2

```java
public class find_maxnumber {
   public static int max(int[] m) {
      int n = 0;
      int max_number = m[0];
      while (n<m.length){
         if (m[n]>max_number){
            max_number = m[n];
         }
         n = n+1;
      }       
      return max_number;
   }
   public static void main(String[] args) {
      int[] numbers = new int[]{9, 2, 15, 2, 22, 10, 6};
   System.out.println(max(numbers));
   }
}
```

## Exercise 3

```java
public class find_maxnumber {
   public static int max(int[] m) {
      int max_number = m[0];
      for (int n = 0,; n<m.length; n += 1){
         if (m[n]>max_number){
            max_number = m[n];
         }
      }
      return max_number;
   }
   public static void main(String[] args) {
      int[] numbers = new int[]{9, 2, 15, 2, 22, 10, 6};
      System.out.println(max(numbers));
   }
}
```

## Exercise 4

```java
public class BreakContinue {
  public static void windowPosSum(int[] a, int n) {
    /** your code here */ 
    int[] result = new int[a.length];
    for (int i=0 ; i<a.length; i += 1){
      if (a[i]>0){
        for (int k=i; k-i<=n; k += 1){
          if (k >= a.length){
            break;  
          }
          result[i] += a[k];         
        }
      }else{
        result[i] = a[i];
      }
    }
     System.out.println(java.util.Arrays.toString(result));
  }

  public static void main(String[] args) {
    int[] a = {1, 2, -3, 4, 5, 4};
    int n = 3;
    windowPosSum(a, n);

    // Should print 4, 8, -3, 13, 9, 4
    System.out.println(java.util.Arrays.toString(a));
  }
}
```





