class Solution:
    def countPrimes(self, n: int) -> int:
        count, sieve = 0, [True] * n
        for i in range(2, n):
            if sieve[i]:
                count+=1
                for j in range(i*i, n, i):
                    sieve[j] = False
        return count
