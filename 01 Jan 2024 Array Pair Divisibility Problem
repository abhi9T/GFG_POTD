#User function Template for python3

class Solution:
	def canPair(self, nuns, k):
		# Code here
        if len(nums) % 2 != 0:
            return False  # If the number of elements is odd, pairs cannot be formed.

        remainder_count = {}  # To store the count of remainders when divided by k.

        for num in nums:
            remainder = num % k
            remainder_count[remainder] = remainder_count.get(remainder, 0) + 1

        for remainder in remainder_count:
            # If the remainder is 0, there must be an even count of such elements.
            # If the remainder is k//2 (for an even k), there must be an even count of such elements.
            # For other remainders, check if there exists a pair with the complementary remainder.
            if remainder == 0 or (k % 2 == 0 and remainder == k // 2):
                if remainder_count[remainder] % 2 != 0:
                    return False
            else:
                complement = k - remainder
                if complement not in remainder_count or remainder_count[complement] != remainder_count[remainder]:
                    return False

        return True

#{ 
 # Driver Code Starts
#Initial Template for Python 3

if __name__ == '__main__':
	T=int(input())
	for i in range(T):
		n, k = input().split()
		n = int(n)
		k = int(k)
		nums = list(map(int, input().split()))
		ob = Solution()
		ans = ob.canPair(nums, k)
		if(ans):
			print("True")
		else:
			print("False")
# } Driver Code Ends
