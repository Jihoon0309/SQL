https://www.hackerrank.com/challenges/weather-observation-station-19/problem?isFullScreen=true  

Consider P1(a,c) and P2(b,d) to be two points on a 2D plane where (a,b) are the respective minimum and maximum values of Northern Latitude (LAT_N) and (c,d) are the respective minimum and maximum values of Western Longitude (LONG_W) in STATION  

Query the Euclidean Distance between points P1 and P2 and format your answer to display 4 decimal digits.  
(점 사이의 유클리드 거리를 쿼리하고 답의 형식을 지정하여 소수점 이하 자릿수를 표시합니다.)

<img width="338" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/d32a268f-eb37-44b9-9874-bd94805f59f9">  

'''  
SELECT ROUND(SQRT(POW(MAX(LAT_N)-MIN(LAT_N), 2) + POW(MAX(LONG_W)-MIN(LONG_W), 2)), 4)  
FROM STATION  
'''  
