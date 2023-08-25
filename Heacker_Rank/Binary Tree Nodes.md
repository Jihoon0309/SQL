https://www.hackerrank.com/challenges/binary-search-tree-1/problem?isFullScreen=true  

You are given a table, BST, containing two columns: N and P, where N represents the value of a node in Binary Tree, and P is the parent of N.  
(N과 P라는 두 개의 열을 포함하는 테이블 BST가 제공됩니다. 여기서 N은 이진 트리의 노드 값을 나타내고 P는 N의 부모입니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/ec479977-746b-4547-bed0-091352736911)  
Write a query to find the node type of Binary Tree ordered by the value of the node. Output one of the following for each node:  
(노드 값에 따라 정렬된 이진 트리의 노드 유형을 찾는 쿼리를 작성하세요. 각 노드에 대해 다음 중 하나를 출력합니다.)  

Root: If node is root node.  
Leaf: If node is leaf node.  
Inner: If node is neither root nor leaf node.  

<img width="776" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/c327e3c2-b7db-449b-984b-f6167d21a4db">  

&nbsp;

'''  
SELECT N,  
CASE  
　　　WHEN P IS NULL THEN 'Root'  
　　　WHEN N NOT IN (SELECT P FROM BST WHERE P IS NOT NULL) THEN 'Leaf'  
　　　ELSE 'Inner'  
　　　END AS New  
FROM BST  
ORDER BY N  
'''

&nbsp;

WHEN N NOT IN (SELECT P FROM BST WHERE P IS NOT NULL) THEN 'Leaf' 에서 IS NOT NULL을 하지않으면 NULL이 들어있으면 Leaf로 반환하지 않음  
이부분 주의해서 풀었어야함
