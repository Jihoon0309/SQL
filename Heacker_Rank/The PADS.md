[The PADS](https://www.hackerrank.com/challenges/the-pads/problem?isFullScreen=true)https://www.hackerrank.com/challenges/the-pads/problem?isFullScreen=true  

1. Query an alphabetically ordered list of all names in OCCUPATIONS, immediately followed by the first letter of each profession as a parenthetical (i.e.: enclosed in parentheses). For example: AnActorName(A), ADoctorName(D), AProfessorName(P), and ASingerName(S).  
(OCCUPATIONS에 있는 모든 이름의 알파벳순 목록을 쿼리하고 바로 뒤에 각 직업의 첫 글자를 괄호로 묶습니다(예: 괄호로 묶음). 예: AnActorName(A), ADoctorName(D), AProfessorName(P) 및 ASingerName(S).)  

2. Query the number of ocurrences of each occupation in OCCUPATIONS. Sort the occurrences in ascending order, and output them in the following  
format : There are a total of [occupation_count] [occupation]s.  
where [occupation_count] is the number of occurrences of an occupation in OCCUPATIONS and [occupation] is the lowercase occupation name. If more than one Occupation has the same [occupation_count], they should be ordered alphabetically.  
(OCCUPATIONS에서 각 직업의 발생 횟수를 쿼리합니다. 발생을 오름차순으로 정렬하고 다음 형식으로 출력합니다.  
여기서 [occupation_count]는 OCCUPATIONS에서 직업의 발생 횟수이고 [occupation]은 소문자 직업 이름입니다. 둘 이상의 직업이 동일한 [occupation_count]인 경우 알파벳순으로 정렬해야 합니다.)


![image](https://github.com/Jihoon0309/SQL/assets/130656475/015ce854-367d-41e2-96b8-094b26143ed2)  

Sample Output  
  
Ashely(P)  
Christeen(P)  
Jane(A)  
Jenny(D)  
Julia(A)  
Ketty(P)  
Maria(A)  
Meera(S)  
Priya(S)  
Samantha(D)  
There are a total of 2 doctors.  
There are a total of 2 singers.  
There are a total of 3 actors.  
There are a total of 3 professors.  
  
  
'''  
SELECT CONCAT(Name, '(', LEFT(Occupation, 1), ')')  
FROM OCCUPATIONS  
ORDER BY Name;  
  
SELECT CONCAT('There are a total of ', COUNT(Occupation), ' ', LOWER(Occupation), 's.')  
FROM OCCUPATIONS   
GROUP BY Occupation  
ORDER BY COUNT(Occupation), Occupation;  
'''  

CONCAT로 여러개 붙여서 출력가능, LOWER 사용해서 소문자로 출력
