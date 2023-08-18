https://www.hackerrank.com/challenges/occupations/problem?isFullScreen=true  

Pivot the Occupation column in OCCUPATIONS so that each Name is sorted alphabetically and displayed underneath its corresponding Occupation. The output column headers should be Doctor, Professor, Singer, and Actor, respectively.  
(OCCUPATIONS에서 Occupation 열을 피벗하여 각 이름이 알파벳순으로 정렬되고 해당 Occupation 아래에 표시되도록 합니다. 출력 열 머리글은 각각 Doctor, Professor, Singer 및 Actor여야 합니다.
)  
&nbsp;

Note: Print NULL when there are no more names corresponding to an occupation.  
(참고: 직업에 해당하는 이름이 더 이상 없으면 NULL을 인쇄합니다.)  

<img width="861" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/a82ed00f-ab4c-414d-a6a5-80fee0ddad99">  

&nbsp;

'''  
SELECT   
MAX(CASE WHEN Occupation = 'Doctor' THEN Name END) AS Doctor,  
MAX(CASE WHEN Occupation = 'Professor' THEN Name END) AS Professor,  
MAX(CASE WHEN Occupation = 'Singer' THEN Name END) AS Singer,  
MAX(CASE WHEN Occupation = 'Actor' THEN Name END) AS Actor  

FROM (SELECT *, ROW_NUMBER() OVER (PARTITION BY Occupation ORDER BY Name) AS RN  
　　　　FROM OCCUPATIONS) TEMP  
      
GROUP BY RN  
'''
&nbsp;

&nbsp;

Pivot 하는방법  
MAX(CASE WHEN Occupation = 'Doctor' THEN Name END) AS Doctor  
- MAX 사용한 이유 : 1. GROUP BY 사용하기 위해 사용  
  　　　　　　　　　2. 값이 존재하지않으면 NULL을 나타내주기 위해서 사용함  

FROM (SELECT *, ROW_NUMBER() OVER (PARTITION BY OCCUPATION ORDER BY NAME) AS RN  
　　　　FROM OCCUPATIONS) TEMP  
1. ROW_NUMBER() 행에 순서 번호를 할당함
2. OVER (PARTITION BY OCCUPATION ORDER BY NAME) PARTITION를 사용한 이유는 ORDER BY 기준으로 정렬된 값에 고유한 값을 기준으로 번호 할당하기 때문 (그룹단위로 나누어준다고 생각하면 됨)
