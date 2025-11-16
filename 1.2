-- CÂU TRUY VẤN

-- 1. Truy xuất tên của những nhân viên nhỏ hơn 30 tuổi mà có mức lương lớn hơn 10.000 $
SELECT Fname, Lname
FROM EMPLOYEE
WHERE YEAR(CURDATE()) - YEAR(Bdate) < 30 
  AND Salary > 10000;

-- 2. Truy xuất các name của tất cả employee có sex là male trong Department "Research" 
--    mà làm cho ít nhất một project nhiều hơn 10 giờ một tuần
SELECT DISTINCT E.Fname, E.Lname
FROM EMPLOYEE E
JOIN DEPARTMENT D ON E.Dno = D.Dnumber
JOIN WORKS_ON W ON E.Ssn = W.Essn
WHERE E.Sex = 'M' 
  AND D.Dname = 'Research'
  AND W.Hours > 10;

-- 3. Truy xuất tên của nhân viên là manager của phòng ban "Research"
SELECT E.Fname, E.Lname
FROM EMPLOYEE E
JOIN DEPARTMENT D ON E.Ssn = D.Mgr_ssn
WHERE D.Dname = 'Research';

-- 4. Tìm tên của tất cả employee được giám sát trực tiếp bởi manager của phòng ban "Research"
SELECT E.Fname, E.Lname
FROM EMPLOYEE E
WHERE E.Super_ssn = (
    SELECT D.Mgr_ssn
    FROM DEPARTMENT D
    WHERE D.Dname = 'Research'
);

-- 5. Với mỗi project, liệt kê tên project, và tổng số giờ một tuần 
--    mà tất cả nhân viên phải làm cho project đó
SELECT P.Pname, SUM(W.Hours) AS Total_Hours
FROM PROJECT P
LEFT JOIN WORKS_ON W ON P.Pnumber = W.Pno
GROUP BY P.Pnumber, P.Pname;

-- 6. Với mỗi phòng ban, liệt kê tên phòng ban và tên của tất cả các employee 
--    làm việc cho phòng ban đó
SELECT D.Dname, E.Fname, E.Lname
FROM DEPARTMENT D
LEFT JOIN EMPLOYEE E ON D.Dnumber = E.Dno
ORDER BY D.Dname, E.Lname;

-- 7. Liệt kê tên của tất cả employee không làm bất cứ project nào ở "Houston"
SELECT E.Fname, E.Lname
FROM EMPLOYEE E
WHERE E.Ssn NOT IN (
    SELECT W.Essn
    FROM WORKS_ON W
    JOIN PROJECT P ON W.Pno = P.Pnumber
    WHERE P.Plocation = 'Houston'
);

-- 8. Liệt kê tên của tất cả employee làm việc cho tất cả các project ở "Houston"
SELECT E.Fname, E.Lname
FROM EMPLOYEE E
WHERE NOT EXISTS (
    SELECT P.Pnumber
    FROM PROJECT P
    WHERE P.Plocation = 'Houston'
    AND P.Pnumber NOT IN (
        SELECT W.Pno
        FROM WORKS_ON W
        WHERE W.Essn = E.Ssn
    )
);

-- 9. Tìm các employee có tổng số dự án tham gia nhiều nhất trong công ty
SELECT E.Fname, E.Lname, COUNT(W.Pno) AS Project_Count
FROM EMPLOYEE E
JOIN WORKS_ON W ON E.Ssn = W.Essn
GROUP BY E.Ssn, E.Fname, E.Lname
HAVING COUNT(W.Pno) = (
    SELECT MAX(Project_Count)
    FROM (
        SELECT COUNT(Pno) AS Project_Count
        FROM WORKS_ON
        GROUP BY Essn
    ) AS PC
);

-- 10. Liệt kê tên các employee có lương cao nhất trong mỗi phòng ban
SELECT E.Fname, E.Lname, E.Dno, E.Salary
FROM EMPLOYEE E
WHERE E.Salary = (
    SELECT MAX(E2.Salary)
    FROM EMPLOYEE E2
    WHERE E2.Dno = E.Dno
)
ORDER BY E.Dno;

-- 11. Với mỗi phòng ban, tìm các employee có tổng số dự án tham gia nhiều nhất 
--     trong phòng ban đó
SELECT E.Fname, E.Lname, E.Dno, COUNT(W.Pno) AS Project_Count
FROM EMPLOYEE E
JOIN WORKS_ON W ON E.Ssn = W.Essn
GROUP BY E.Ssn, E.Fname, E.Lname, E.Dno
HAVING COUNT(W.Pno) = (
    SELECT MAX(PC.Project_Count)
    FROM (
        SELECT E2.Dno, COUNT(W2.Pno) AS Project_Count
        FROM EMPLOYEE E2
        JOIN WORKS_ON W2 ON E2.Ssn = W2.Essn
        WHERE E2.Dno = E.Dno
        GROUP BY E2.Ssn
    ) AS PC
)
ORDER BY E.Dno;

-- 12. Liệt kê last name của tất cả các manager của các department 
--     nhưng không tham gia project nào
SELECT E.Lname
FROM EMPLOYEE E
JOIN DEPARTMENT D ON E.Ssn = D.Mgr_ssn
WHERE E.Ssn NOT IN (
    SELECT DISTINCT Essn
    FROM WORKS_ON
);
