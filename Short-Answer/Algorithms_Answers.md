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
    def bunnyEars(bunnies):
        if bunnies == 0:
          return 0

        return 2 + bunnyEars(bunnies-1)
    -->
    - This algorithm has a runtime of O(bunnies*bunnies-1) => O(n*n)
