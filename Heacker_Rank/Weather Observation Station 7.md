https://www.hackerrank.com/challenges/weather-observation-station-7/problem?isFullScreen=true  

Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.  
(STATION에서 모음(a, e, i, o, u)으로 끝나는 CITY 이름 목록을 쿼리합니다. 결과는 중복을 포함할 수 없습니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/40375e1d-0406-44e0-a2c0-4eae2aa1492b)  

'''  
SELECT DISTINCT CITY  
FROM STATION  
WHERE (CITY LIKE '%a' or  
　　　CITY LIKE '%e' or  
　　　CITY LIKE '%i' or  
　　　CITY LIKE '%o' or  
　　　CITY LIKE '%u')  
'''

