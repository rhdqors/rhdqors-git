## MYSQL 데이터형식





**1. 정수타입 **

* Ttinyint(1바이트)
* smallint(2바이트)
* int(4바이트)
* bigint(8바이트)





**2. 실수타입 **

* float(4바이트)
* double(8바이트)
* decimal(15.3)





**3. 날짜시간타입**

* date
* time
* datetime





**4. 문자열**

* 





**unicode**

* char(1000)
  * 영문 1글자, 한글 1글자 실제 바이트수 다르다 ( 10글자 입력 + 90글자 비어있음)



* varchar(100)
  * 영문 1글자, 한글 1글자 실제 바이트수 다르다 ( 10글자 입력 )





---

# 오늘의 메모

-- 이름에 le 포함한 사원들만 부서명 조회 ---> mysql에서 정의한 join 기본 틀
select first_name 사원명, e.department_id 부서코드, department_name 부서명
from employees e inner join departments d on e.department_id = d.department_id
where instr(first_name, 'le') >= 1 -- first_name like '%le%'
order by 1;

-- 이름에 le 포함한 사원들만 부서명 조회 ---> 동작은 똑같이 한다. 하지만 위에것을 쓰도록
select first_name 사원명, e.department_id 부서코드, department_name 부서명
from employees e inner join departments d 
where  e.department_id = d.department_id
and instr(first_name, 'le') >= 1 -- first_name like '%le%'
order by 1;

