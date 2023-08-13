https://www.hackerrank.com/challenges/weather-observation-station-11/problem?isFullScreen=true  

Query the list of CITY names from STATION that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates.  
(STATION에서 모음으로 시작하지 않거나 모음으로 끝나지 않는 CITY 이름 목록을 쿼리합니다. 결과는 중복을 포함할 수 없습니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/fa1b1636-f714-487d-a432-7655f13e062e)  

'''  
SELECT DISTINCT CITY  
FROM STATION  
WHERE CITY REGEXP '^[^aeiou]' OR CITY REGEXP '[^aeiou]$'   
'''
