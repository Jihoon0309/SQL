https://www.hackerrank.com/challenges/weather-observation-station-10/problem?isFullScreen=true  

Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates.  
(STATION에서 모음으로 끝나지 않는 CITY 이름 목록을 쿼리합니다. 결과는 중복을 포함할 수 없습니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/ccf73bfc-8d3f-4179-b6d8-387cc7f9d8bb)  

'''  
SELECT DISTINCT CITY  
FROM STATION  
WHERE CITY REGEXP '[^aeiou]$'  
'''
