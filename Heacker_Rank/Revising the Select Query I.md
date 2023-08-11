https://www.hackerrank.com/challenges/revising-the-select-query/problem?isFullScreen=true</br>

Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.</br>
(인구가 100,000명 이상인 CITY 테이블의 모든 미국 도시에 대한 모든 열을 쿼리합니다. 미국의 CountryCode는 USA입니다.)

The CITY table is described as follows:</br>

![image](https://github.com/Jihoon0309/SQL/assets/130656475/aff80473-5553-4d93-90f4-6fe8e8cf3736)





SQL CODE
</br>
'''</br>
SELECT *</br>
FROM CITY</br>
WHERE POPULATION >= 100000</br>
AND COUNTRYCODE = 'USA'</br>
'''
