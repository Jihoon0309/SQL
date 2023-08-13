https://www.hackerrank.com/challenges/japanese-cities-attributes/problem?isFullScreen=true  

Query all attributes of every Japanese city in the CITY table. The COUNTRYCODE for Japan is JPN.  
(CITY 테이블에 있는 모든 일본 도시의 모든 속성을 쿼리합니다. 일본의 국가 코드는 JPN입니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/36ed0137-3aab-4fb7-9305-9d8592f38e42)  

'''  
SELECT *  
FROM CITY  
WHERE COUNTRYCODE = 'JPN'  
'''
