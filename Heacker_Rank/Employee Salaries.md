https://www.hackerrank.com/challenges/salary-of-employees/problem?isFullScreen=true&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen  

Write a query that prints a list of employee names (i.e.: the name attribute) for employees in Employee having a salary greater than $2000 per month who have been employees for less than 10 months. Sort your result by ascending employee_id.  
(월급이 $2000 이상이고 근무 기간이 10개월 미만인 Employee의 직원에 대한 직원 이름(즉, 이름 속성) 목록을 인쇄하는 쿼리를 작성합니다. employee_id를 오름차순으로 결과를 정렬합니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/9eb13370-ba21-4c9b-b94f-84152c1b66d1)  


'''  
SELECT name  
FROM Employee  
WHERE salary>=2000 AND  
　　　months < 10  
'''
