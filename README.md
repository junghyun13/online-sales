# online-sales
# python
# In N and M, the number of goods and the number of customers are written, and the price that customers want is input, and the lowest price and profit that can make the maximum profit are output. N과 M에는 물건의 수와 고객의 수가 적혀있고 고객들이 원하는 가격을 입력하고 최대 수익을 올릴수 있는 가장 낮은 가격과 수익을 출력한다.
import sys
input=sys.stdin.readline
N,M=map(int,input().split())
add=0
people=[]
price=0
for i in range(M):
    people.append(int(input()))
if N>=M:
    people.sort()
    check=True
    loop=M
else:
    people.sort(reverse=True)
    check=False
    loop=N
for i in range(loop):
    if check==True:
        cnt=M-i
    else:
        cnt=i+1
    if sum<people[i]*cnt:
        price=people[i]
        add=people[i]*cnt
print(price,add)
# input--> 5 4   2 8 10 7
# result--> 7 21
