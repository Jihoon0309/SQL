https://www.hackerrank.com/challenges/revising-the-select-query-2/problem?isFullScreen=true</br>

Query the NAME field for all American cities in the CITY table with populations larger than 120000. The CountryCode for America is USA.</br>
(인구가 120000명 이상인 CITY 테이블의 모든 미국 도시에 대한 NAME 필드를 쿼리합니다. 미국의 CountryCode는 USA입니다.)</br>

The CITY table is described as follows:</br>
![image](https://github.com/Jihoon0309/SQL/assets/130656475/7ffff517-4b07-4870-809c-c6da946e5691)


'''</br>
SELECT NAME</br>
FROM CITY</br>
WHERE POPULATION >= 120000</br>
AND COUNTRYCODE = 'USA'</br>
'''
