Add your answers to the Algorithms exercises here.

Exercise 1:
  A:
    <!-- 
      a = 0
      while (a < n * n * n):
        a = a + n * n 
    -->
    - We're incrementing a n x n (n^2) times while a is less than n x n x n (n^3)
    - Therefore, we can divide n^3 by n^2 (subtract exponent) which leaves us with n^1 --> n
    - this loop has a runtime of n

  
  B:
    <!-- 
    sum = 0
      for i in range(n):                    => O(n)
        i += 1                              => O(1)
        for j in range(i + 1, n):           => O(n - i+1) => O(n - i) => O(n)
        j += 1                              => O(1)
          for k in range(j + 1, n):         => O(n - j+1) => O(n - j) => O(n)
            k += 1                          => O(1)
            for l in range(k + 1, 10 + k):  => O(10+k - k+1) => O(k + 10) => O(k) 
              l += 1                        => O(1)
              sum += 1                      => O(1)
    -->
    - This algorithm hs a runtime of O(k * n^3)

  C:
    <!-- 
    def bunnyEars(bunnies):           => O(n)
      if bunnies == 0:
        return 0
      return 2 + bunnyEars(bunnies-1) => O(n-1)
    -->
    
    - This algorithm has a runtime of O(bunnies*bunnies-1) => O(n*2)

Exercise 2:

-- divide & conquer technique --

1. n = number of floors to search
2. start at the middle floor and drop an egg

if the egg breaks:
  - go to the middle floor of the bottom half of the building
  - n = bottom half
  - repeat step 2

if the egg doesn't break:
  - go to the middle floor of the top half of the building
  - n = top half
  - repeat step 2

3. repeat until only 1 floor remains and return that floor

runtime complexity is O(log n)