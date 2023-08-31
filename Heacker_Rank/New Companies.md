https://www.hackerrank.com/challenges/the-company/problem?isFullScreen=true  

Given the table schemas below, write a query to print the company_code, founder name, total number of lead managers, total number of senior managers, total number of managers, and total number of employees. Order your output by ascending company_code.  
(
아래 테이블 스키마가 주어지면 회사_코드, 설립자 이름, 총 리드 관리자 수, 총 고위 관리자 수, 총 관리자 수 및 총 직원 수를 인쇄하는 쿼리를 작성하세요. company_code를 오름차순으로 출력을 정렬하십시오.)  

<img width="891" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/83754c58-f895-4418-84ae-fc521462a81d">  

<img width="889" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/3f9561d4-5be4-41ba-86f4-0a0d1650d2de">  


&nbsp;

'''  
SELECT C.company_code, C.founder, COUNT(DISTINCT E.lead_manager_code), COUNT(DISTINCT E.senior_manager_code),  
　　　　　COUNT(DISTINCT E.manager_code), COUNT(DISTINCT E.employee_code)  
FROM Company as C INNER JOIN Employee as E ON C.company_code = E.company_code  
GROUP BY C.company_code, founder  
ORDER BY C.company_code  
'''  
