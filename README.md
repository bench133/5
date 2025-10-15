# 5
mone
n = int(input())
arrays = []
sizes = []
 
for _ in range(n):
    elements = list(map(int, input().split()))
    arrays.append(elements[:])
    sizes.append(len(elements))
 
m = int(input())
for _ in range(m):
    q = input().split()
    if q[0] == '+':
        x = int(q[1]) - 1
        e = int(q[2])
        arrays[x].append(e)         
        sizes[x] += 1
    elif q[0] == '-':
        x = int(q[1]) - 1
        arrays[x].pop()             
        sizes[x] -= 1
    elif q[0] == '?':
        x = int(q[1]) - 1
        y = int(q[2]) - 1
        print(arrays[x][y], flush=True)
