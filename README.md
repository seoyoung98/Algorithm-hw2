# Algorithm-hw2
## 최단 경로(Shortest Path) 문제
주어진 가중치 그래프에서 어느 한 출발점에서 또 다른 도착점까지의 최단 경로를 찾는 문제이다.

### 최단 경로를 찾는 알고리즘 - 다익스트라(Dijkstra)
 - 특정한 하나의 정점에서 다른 모든 정점으로 가는 최단 경로
 - 최단 거리는 여러 개의 최단 거리로 이루어져 있음
 - 하나의 최단 거리를 구할 때 그 이전까지 구했던 최단 거리 정보를 그대로 사용
 - 정렬을 사용하고 그 중 가장 작은 것을 사용
 - 현재까지 알고있던 최단 경로를 계속해서 갱신

### 작동 과정
  1. 출발 노드를 설정
  2. 출발 노드를 기준으로 각 노드의 최소 비용을 저장
  3. 방문하지 않은 노드 중 가장 비용이 적은 노드 선택
  4. 해당 노드를 거쳐서 특정한 노드로 가는 경우를 고려하여 최소 비용을 갱신
    <br> ex. 1-> 4-> 3 : 4, 1-> 3 : 5 일때 4가 5보다 작으므로 4로 갱신
         <br>   1-> 4-> 5-> 3 : 3 이면 또 최소이므로 갱신
  5. 3~4번을 반복 

#### Shortest Path(G,V)
