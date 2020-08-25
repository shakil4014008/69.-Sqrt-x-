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
 
