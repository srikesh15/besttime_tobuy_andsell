# besttime_tobuy_andsell
class Solution:
    def max_profit(prices):
        l, r = 0, 1    # left=buy, right=sell
        maxP = 0

        while r < len(prices):
            # profitable?
            if prices[l] < prices[r]:
                profit = prices[r] - prices[l]
                maxP = max(maxP, profit)
            else:
                l = r
            r = r + 1
        return maxP


    prices = list(map(int,input().split()))

