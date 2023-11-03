https://www.hackerrank.com/challenges/full-score/problem?isFullScreen=true  

Julia just finished conducting a coding contest, and she needs your help assembling the leaderboard!  
Write a query to print the respective hacker_id and name of hackers who achieved full scores for more than one challenge.  
Order your output in descending order by the total number of challenges in which the hacker earned a full score.  
If more than one hacker received full scores in same number of challenges, then sort them by ascending hacker_id.  
(Julia는 방금 코딩 콘테스트를 마쳤습니다.  
순위표를 구성하는 데 여러분의 도움이 필요합니다!  
두 개 이상의 챌린지에서 만점을 달성한 해커의 이름과 hacker_id를 인쇄하는 쿼리를 작성하세요.  
해커가 만점을 획득한 총 챌린지 수를 기준으로 내림차순으로 출력을 정렬하세요. 두 명 이상의 해커가 동일한 수의 챌린지에서 만점을 받은 경우 hacker_id를 오름차순으로 정렬합니다.)  

<img width="828" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/c86894c9-2636-4409-a04c-2f1856936842">
<img width="830" alt="image" src="https://github.com/Jihoon0309/SQL/assets/130656475/14e6629b-6c78-479f-b1b5-0e9f4e76f71e">  

'''  
SELECT H.hacker_id, H.name  
FROM Submissions AS S  
    JOIN Challenges AS C ON S.challenge_id = C.challenge_id  
    JOIN Hackers AS H ON S.hacker_id = H.hacker_id  
    JOIN Difficulty AS D ON C.difficulty_level = D.difficulty_level  
WHERE D.score = S.score AND D.difficulty_level = C.difficulty_level  
GROUP BY H.hacker_id, H.name  
HAVING COUNT(H.hacker_id) > 1  
ORDER BY COUNT(*) DESC, H.hacker_id  
'''  
