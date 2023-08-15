https://www.hackerrank.com/challenges/more-than-75-marks/problem?isFullScreen=true  

Query the Name of any student in STUDENTS who scored higher than  Marks. Order your output by the last three characters of each name.  
If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.  
(STUDENTS에서 75점보다 높은 점수를 받은 학생의 이름을 쿼리하십시오. 각 이름의 마지막 세 문자로 출력을 정렬하십시오. 두 명 이상의 학생 모두 이름이 마지막 세 글자로 끝나는 경우(예: Bobby, Robby 등) ID를 오름차순으로 2차 정렬합니다.)  

![image](https://github.com/Jihoon0309/SQL/assets/130656475/ec238a56-f979-4ec8-b7e2-7bc2f31ec5fb)  


'''  
SELECT Name  
FROM STUDENTS  
WHERE Marks>75  
ORDER BY RIGHT (Name, 3), ID  
'''
