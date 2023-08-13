https://www.hackerrank.com/challenges/weather-observation-station-9/problem?isFullScreen=true  

Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.  
(STATION에서 모음으로 시작하지 않는 CITY 이름 목록을 쿼리합니다. 결과는 중복을 포함할 수 없습니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/7a92e081-e072-401a-a509-27ca20d85194)  

'''  
SELECT DISTINCT CITY  
FROM STATION  
WHERE CITY REGEXP '^[^aeiou]'  
'''
