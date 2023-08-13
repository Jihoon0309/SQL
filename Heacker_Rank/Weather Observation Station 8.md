https://www.hackerrank.com/challenges/weather-observation-station-8/problem?isFullScreen=true  

Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.  
(모음(즉, a, e, i, o 및 u)이 첫 문자와 마지막 문자로 모두 있는 STATION의 CITY 이름 목록을 쿼리합니다. 결과는 중복을 포함할 수 없습니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/477d72f6-2ab2-4800-939f-cd8726261e55)  

'''  
SELECT CITY  
FROM STATION  
WHERE CITY REGEXP '^[aeiou]' AND CITY REGEXP '[aeiou]$'  
'''  

SQL에서도 정규식 사용이 가능함
