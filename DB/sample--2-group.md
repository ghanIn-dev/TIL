# Sample -2 Group

종료일자가 없다는 의미로 9999-01-01 을 사용했음을 참고하고 실습한다.

* **현재 일하는 업무별 직원의 수를 구하시오**

  ```
  SELECT TITLE,COUNT(*)
  FROM TITLES
  WHERE TO_DATE='9999-01-01'
  GROUP BY TITLE
  ORDER BY TITLE;
  ```

* **남여 직원수를 구하되 M은 '남' F는 '여'로 출력하시오**

* ```
  SELECT IF(GENDER='M','남','여')GENDER,COUNT(*)
  FROM EMPLOYEES
  GROUP BY GENDER;
  ```

* **부서별 현재 인원수가 많은 순서로 출력하시오**

  ```
  SELECT DEPT_NO, COUNT(*) AS CNT
  FROM DEPT_EMP
  WHERE TO_DATE='9999-01-01'
  GROUP BY DEPT_NO
  ORDER BY CNT DESC;
  ```

* **부서 이동이 많은 직원순으로 출력하시오**

  ```
  SELECT EMP_NO, COUNT(*) CNT
  FROM DEPT_EMP
  GROUP BY EMP_NO
  HAVING COUNT(*)>1
  ORDER BY CNT DESC
  ```

* **부서별 현재 인원수가 15000명 이상인 부서를 구하시오**

* ```
  SELECT DEPT_NO, COUNT(*) CNT
  FROM DEPT_EMP
  WHERE TO_DATE='9999-01-01'
  GROUP BY DEPT_EMP
  HAVING CNT>15000
  ORDER BY CNT DESC
  ```

* **직원들의 부서 이동 과정을 출력하시오**

* ```
  SELECT EMP_NO, GROUP_CONCAT(DEPT_NO SEPARATOR '>') PATH
  FROM DEPT_EMP
  GROUP BY EMP_NO
  HAVING COUNT(*)>1
  ```

  우선 개인별로 그룹화한 후 GROUP\_CONCAT\(그룹으로 지정된 데이터들을 지정한 구분자를 이용하여 하나의 문자열로 만든다\)을 사용한다.

