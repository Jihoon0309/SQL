https://www.hackerrank.com/challenges/weather-observation-station-4/problem?isFullScreen=true  

Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.  
(테이블의 총 CITY 항목 수와 테이블의 개별 CITY 항목 수 간의 차이를 찾으십시오.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/bbceae8c-bbac-4694-a27e-d7b0da85d582)  

'''  
SELECT COUNT(CITY) - COUNT(DISTINCT CITY)  
FROM STATION  
'''
