```C#
      public int MySqrt(int x) {
      
       if(x < 2) return x;
        
        int left = (int)Math.Pow(Math.E, .5 * Math.Log(x));
        int right = left +1;
        
        return (long)right * right > x ? left : right; 
    }
```

## Complexity Analysis

* Time Complexity: O(1)
* Space Complexity: O(1)


Solution 2:

Algorithm
If x < 2, return x.
Set the left boundary to 2, and the right boundary to x / 2.
While left <= right:
      Take num = (left + right) / 2 as a guess. Compute num * num and compare it with x:
            If num * num > x, move the right boundary right = pivot -1
            Else, if num * num < x, move the left boundary left = pivot + 1
            Otherwise num * num == x, the integer square root is here, let's return it
Return right


```C#
        public int MySqrt(int x) {
      if(x < 2) return x;
        
      long num; 
      int pivot, left=2, right = x/2;
      while(left <= right){
          pivot = left + (right - left) /2;
          //Console.WriteLine(pivot);
          num = (long)pivot * pivot;
          if(num > x) right = pivot -1;        
          else if(num < x) {left= pivot + 1;
          Console.WriteLine(num);}
          else return pivot;
      }
        
        return right;
      
    }
```

## Complexity Analysis

* Time Complexity: O(logN)
* Space Complexity: O(1)
 
