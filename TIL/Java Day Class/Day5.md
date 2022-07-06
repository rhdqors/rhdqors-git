# Thread 

```
class A extends Thread{
public void run () {
상속 오버라이딩 멀티 스레드 실행 코드
  }
}

main(){
Thread t1 = new A ();
t1.start(); --> 상속, 호출/run 실행
system.out.println ();
}
```

> Thread 클래스 상속
>
> run 메소드 오버라이딩
>
> Thread 하위클래스 객체 생성
>
> start 호출



```
class A extends C implements Runnable{
public void run(){
상속 오버라이딩
  }
}

main() {
A a1 = new A();
Thread ta1 = new Thread(a1);
ta1.start();  --> 상속, 호출/run 실행
}
```

>Runnable 인터페이스 상속
>
>run 메소드 오버라이딩
>
>Thread 하위클래스 객체 생성
>
>start 호출

