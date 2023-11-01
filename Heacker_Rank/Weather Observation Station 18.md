https://www.hackerrank.com/challenges/weather-observation-station-18/problem?isFullScreen=true  

Consider  and  to be two points on a 2D plane.  

 happens to equal the minimum value in Northern Latitude (LAT_N in STATION).  
 happens to equal the minimum value in Western Longitude (LONG_W in STATION).  
 happens to equal the maximum value in Northern Latitude (LAT_N in STATION).  
 happens to equal the maximum value in Western Longitude (LONG_W in STATION).  
Query the Manhattan Distance between points  and  and round it to a scale of  decimal places.  
(점 사이의 맨해튼 거리를 쿼리하고 소수점 이하 자릿수로 반올림합니다.)  

<img width="337" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/50286329-10f1-49e9-b34b-ddd28737d8cc">  

'''  
SELECT ROUND(ABS(MAX(LAT_N)-MIN(LAT_N)) + ABS(MAX(LONG_W)-MIN(LONG_W)), 4)  
FROM STATION  
'''  

우리가 평소에 아는 공식인 유클리드 거리와 다르게 맨허튼 거리 공식은  
<img width="347" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/15451e36-dcac-42d0-8222-aebb74645eb0">  
이렇게 구해야 함
