https://www.hackerrank.com/challenges/weather-observation-station-5/problem?isFullScreen=true  

Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name).  
If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.  
(가장 짧은 CITY 이름과 가장 긴 CITY 이름 및 각각의 길이(예: 이름의 문자 수)를 사용하여 STATION의 두 도시를 쿼리합니다.  
가장 작은 도시 또는 가장 큰 도시가 둘 이상인 경우 알파벳순으로 정렬할 때 먼저 오는 도시를 선택하십시오.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/93cfbf4a-4b7d-42aa-8e33-54e1c8e84b2e)  

Sample Output  
ABC 3  
PQRS 4  


'''  
SELECT CITY, LENGTH(CITY)  
FROM STATION  
ORDER BY LENGTH(CITY), CITY  
LIMIT 1;  

SELECT CITY, LENGTH(CITY)  
FROM STATION  
ORDER BY LENGTH(CITY) DESC, CITY DESC  
LIMIT 1;  
'''
