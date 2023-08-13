https://www.hackerrank.com/challenges/japanese-cities-name/problem?isFullScreen=true  

Query the names of all the Japanese cities in the CITY table. The COUNTRYCODE for Japan is JPN.  
(CITY 테이블에 있는 모든 일본 도시의 이름을 쿼리합니다. 일본의 국가 코드는 JPN입니다)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/a4324197-5a75-4b5d-b80b-fd55c8bd62c6)  

'''  
SELECT NAME  
FROM CITY  
WHERE COUNTRYCODE = 'JPN'  
'''
