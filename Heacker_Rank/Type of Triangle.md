https://www.hackerrank.com/challenges/what-type-of-triangle/problem?isFullScreen=true  

Write a query identifying the type of each record in the TRIANGLES table using its three side lengths. Output one of the following statements for each record in the table:  
(세 변의 길이를 사용하여 TRIANGLES 테이블의 각 레코드 유형을 식별하는 쿼리를 작성하십시오. 테이블의 각 레코드에 대해 다음 문 중 하나를 출력합니다.)  

Equilateral : It's a triangle with  sides of equal length.  
(Equilateral : 변의 길이가 같은 삼각형입니다.)  
Isosceles : It's a triangle with  sides of equal length.  
(Isosceles : 변의 길이가 같은 삼각형입니다.)  
Scalene : It's a triangle with  sides of differing lengths.  
(Scalene : 변의 길이가 다른 삼각형입니다.)  
Not A Triangle : The given values of A, B, and C don't form a triangle.  
(Not A Triangle : A, B, C의 주어진 값이 삼각형을 형성하지 않습니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/7f6071e2-3c2b-4aa9-926b-87061d5b0554)  


'''  
SELECT  
CASE  
　　　WHEN A=B AND B=C THEN 'Equilateral'  
　　　WHEN A>=B+C OR B>=A+C OR C>=A+B THEN 'Not A Triangle'  
　　　WHEN A=B OR A=C OR B=C THEN 'Isosceles'  
　　　ELSE 'Scalene'  
END  
FROM TRIANGLES  
'''

  
  
CASE - WHEN 문은 순서대로 조건을 만족하게되면 뒤에 조건도 만족하더라도 선행되는 조건을 채택함  
(이 부분 생각해서 풀어야했음)
