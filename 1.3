-- CÂU LỆNH CẬP NHẬT DỮ LIỆU

-- 1. Nhân viên có mã là "123456789" thay đổi địa chỉ thành "123 Lý Thường Kiệt F.14 Q.10"
UPDATE EMPLOYEE
SET Address = '123 Lý Thường Kiệt F.14 Q.10'
WHERE Ssn = '123456789';

-- 2. Mối quan hệ của nhân viên "Franklin" với người phụ thuộc "Joy" thay đổi thành "Friend"
UPDATE DEPENDENT
SET Relationship = 'Friend'
WHERE Essn = (
    SELECT Ssn
    FROM EMPLOYEE
    WHERE Fname = 'Franklin'
)
AND Dependent_name = 'Joy';

-- 3. Tất cả nhân viên của phòng ban có ít nhất một vị trí ở "Houston" được tăng lương gấp đôi
UPDATE EMPLOYEE
SET Salary = Salary * 2
WHERE Dno IN (
    SELECT DISTINCT Dnumber
    FROM DEPT_LOCATIONS
    WHERE Dlocation = 'Houston'
);

-- 4. Trừ 5% lương cho các nhân viên có tổng số dự án tham gia ít hơn 2
UPDATE EMPLOYEE
SET Salary = Salary * 0.95
WHERE Ssn IN (
    SELECT Essn
    FROM (
        SELECT Essn, COUNT(Pno) AS Project_Count
        FROM WORKS_ON
        GROUP BY Essn
        HAVING COUNT(Pno) < 2
    ) AS EmpProjects
)
OR Ssn NOT IN (
    SELECT DISTINCT Essn
    FROM WORKS_ON
);
