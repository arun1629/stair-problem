#stair problem
'''there n stairs , a person standing at the bottom wants to reach the top. 
the person can climb either 1 or 2 stairs at a time.Count the number of ways,
the person can reach the top'''

def no_ways_to_reach_top(n):
  if n<= 2:
    return n
  f1 = 1
  f2 = 2
  for i in range(2,n):
    ways = f1+f2
    f1 = f2
    f2 = ways
  return ways

