from collections import deque
n, e = map(int, input().split())
g = {i: [] for i in range(n)}
ind = [0]*n
for _ in range(e):
    u, v = map(int, input().split())
    g[u].append(v)
    ind[v] += 1
q = deque([i for i in range(n) if ind[i] == 0])
res = []
while q:
    u = q.popleft()
    res.append(u)
    for v in g[u]:
        ind[v] -= 1
        if ind[v] == 0:
            q.append(v)
print(res if len(res) == n else "Cycle")
