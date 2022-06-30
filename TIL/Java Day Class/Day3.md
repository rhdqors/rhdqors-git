# 형변환





> 자동 형변환

- 하위 객체 생성하여 상위클래스 변환

- 서로 다른 타입의 객체들을 사용시 타입 1가지 통일 필요



> 명시적 형변환

- 상위클래스 내부 포함된 변수만 사용 제한 -> (하위클래스 포함 변수를 쓰고싶을 때 자동 형변환)



---

class 타이어

class 한국타이어 extands 타이어

class 금호타이어 extands 타이어

타이어 t = new 한국타이어(); --> 자동 형변환 ( 다른 두 객체의 값을 매치)

타이어 t = new 금호타이어();

---

A a1 = new A();

> class A { i j ma(); 
>
> A a2 = new B(); -> 자동 형변환



A a3 = new C(); -> 자동 형변환   

A a4 = new D(); -> 자동 형변환

B b1 = new C(); -> error (상속x)   





# Overriding

- class A { ma(){x;} ,mc(){} }             

  - class B esxtends A { mb(){} ma(){x+y;} }      

  - 위 class A의 ma() 메서드를 아래 class B에서 새롭게 값을 지정 = 오버라이딩

​    

B b1 = new B();

b1.ma();   --->  class B의 x+y값이 나온다

​    

​    