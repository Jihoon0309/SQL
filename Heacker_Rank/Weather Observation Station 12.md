https://www.hackerrank.com/challenges/weather-observation-station-12/problem?isFullScreen=true  

Query the list of CITY names from STATION that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.  
(STATION에서 모음으로 시작하지 않고 모음으로 끝나지 않는 CITY 이름 목록을 쿼리합니다. 결과는 중복을 포함할 수 없습니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/c96fab16-51c1-4b03-a3df-4da9dd8bc96c)  

'''  
SELECT DISTINCT CITY  
FROM STATION  
WHERE CITY REGEXP '^[^aeiou]' AND CITY REGEXP '[^aeiou]$'  
'''
