https://www.hackerrank.com/challenges/weather-observation-station-3/problem?isFullScreen=true  

Query a list of CITY names from STATION for cities that have an even ID number. Print the results in any order, but exclude duplicates from the answer.  
(ID 번호가 짝수인 도시에 대해 STATION에서 CITY 이름 목록을 쿼리합니다. 결과를 순서에 관계없이 인쇄하되 답에서 중복 항목을 제외합니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/6f81b1a1-9925-4979-b46f-14cdc7719a32)  

'''  
SELECT DISTINCT CITY  
FROM STATION  
WHERE ID%2=0  
'''
