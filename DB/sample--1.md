# Sample - 1 기본적인 sql 구문

* **직원의 이름을 순서대로 리스트 출력해라**

  ```
  SELECT *    
  FROM EMPLOYEES
  ORDER BY FIRST_NAME,LAST_NAME
  ```

* **직원 중 나이가 가장 많은 사람의 나이는 몇살인가?**

  ```
  SELECT TIMESTAMPDIFF(YEAR,MIN(BIRTH_DATE),NOW())
  FROM EMPLOYEES;
  ```

  NOW는 현재 시간을 가져오는 함수
  TIMESTAMPDIFF는 시간의 차이를 구하는 함수 -&gt; 파라미터 : \(단위,1,2\)

* **가장 최근에 입사한 사람 100명 출력**

* ```
    SELECT *
    FROM EMPLOYEES
    ORDER BY HIRE_DATE DESC
    LIMIT 100
  ```


limit은 데이터의 개수를 제한하는 명령어로 뒤에 정수가 1개일 경우 갯수를 의미하고 정수가 2개일 경우 순서와 갯수를 의미함 
  따라서 limit\(100,10\)의 경우 100부터 110까지의 데이터가 조회 됨

* **1999년에 입사한 직원 중 여자직원의 리스트**

* ```
  SELECT *
  FROM EMPLOYEES
  WHERE YEAR(HIRE_DATE)=1999 AND GENDER='F';
  ```

  조건에 따라 and와 or을 사용할 수 있다

* **1998년이나 1999년에 입사한 남자 직원의 수를 구하시오**

* ```
  SELECT COUNT(*)
  FROM EMPLOYEES
  WHERE (YEAR(HIRE_DATE)=1998 OR YEAR(HIRE_DATE)=1999) AND GENDER='M';
  ```

  COUNT\(\) 함수는 GROUP BY 에 있는 대상을 기본으로 하며 GROUP BY 절이 없을 경우 전체를 대상으로 한다


* **1995년 부터 1999년까지 입사한 직원의 수**

* ```
  SELECT COUNT(*)
  FROM EMPLOYEES
  WHERE YEAR(HIRE_DATE) BETWEEN 1995 AND 1999
  ```

* **1995, 1997, 1999년에 입사한 직원의 평균 나이를 구하시오**

* ```
  SELECT AVG(TIMESTAMPDIFF(YEAR,BIRTH_DATE,NOW())
  FROM EMPLOYEES
  WHERE YEAR(HIRE_DATE) IN (1995,1997,1999);
  ```

* **성\(last\_name\)이 Senzako, Pettis, Henseler인 직원을 출력하시오.**

* ```
  SELECT *
  FROM EMPLOYEES
  WHERE LAST_NAME IN ('Senzako', 'Pettis', 'Henseler');
  ```


