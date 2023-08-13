https://www.hackerrank.com/challenges/weather-observation-station-6/problem?isFullScreen=true  

Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.  
(STATION에서 모음(예: a, e, i, o 또는 u)으로 시작하는 CITY 이름 목록을 쿼리합니다. 결과는 중복을 포함할 수 없습니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/8eeea55a-29c0-41d7-9430-87868c2cfca0)  

'''  
SELECT CITY  
FROM STATION  
WHERE (CITY LIKE 'a%' or   
　　　CITY LIKE 'e%' or   
　　　CITY LIKE 'i%' or   
　　　CITY LIKE 'o%' or   
　　　CITY LIKE 'u%');   
'''
