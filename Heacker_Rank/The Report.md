https://www.hackerrank.com/challenges/the-report/problem?isFullScreen=true  

You are given two tables: Students and Grades. Students contains three columns ID, Name and Marks.  
<img width="366" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/5b991f97-84e9-48db-b191-0dfe3ef02f8c">

Grades contains the following data:  
<img width="324" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/2dbd419b-9dce-4958-8ca2-d0ef67979354">

Ketty gives Eve a task to generate a report containing three columns: Name, Grade and Mark. Ketty doesn't want the NAMES of those students who received a grade lower than 8.  
The report must be in descending order by grade -- i.e. higher grades are entered first. If there is more than one student with the same grade (8-10) assigned to them, order those particular students by their name alphabetically.  
Finally, if the grade is lower than 8, use "NULL" as their name and list them by their grades in descending order. If there is more than one student with the same grade (1-7) assigned to them, order those particular students by their marks in ascending order.  

(Ketty는 Eve에게 이름, 등급, 마크라는 세 개의 열이 포함된 보고서를 생성하는 작업을 제공합니다. Ketty는 8점 미만의 성적을 받은 학생의 이름을 원하지 않습니다.  
보고서는 학년별로 내림차순이어야 합니다. 즉, 높은 성적이 먼저 입력됩니다. 동일한 학년(8-10)을 가진 학생이 두 명 이상인 경우 해당 학생의 이름을 알파벳순으로 정렬합니다.  
마지막으로 성적이 8점 이하인 경우에는 "NULL"을 이름으로 사용하고 성적순으로 내림차순으로 나열한다. 동일한 학년(1-7)을 배정받은 학생이 두 명 이상인 경우 해당 학생의 성적을 기준으로 오름차순으로 정렬합니다.)


'''  
SELECT IF(G.Grade < 8, NULL, S.Name), G.Grade, S.Marks  
FROM Students AS S  
    JOIN Grades AS G ON S.Marks BETWEEN G.Min_Mark AND G.Max_Mark  
ORDER BY G.Grade DESC, S.Name, S.Marks  
'''
