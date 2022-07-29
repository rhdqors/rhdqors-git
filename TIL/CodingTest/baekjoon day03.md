## a+b-5

```jsx
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
	
		Scanner sc = new Scanner(System.in);
		
		while(true) {
		int a = sc.nextInt(); //n개로 이루어진
		int b = sc.nextInt(); //x보다 작은 수 찾기
			
		if(a == 0) {
			break;
		}
		System.out.println(a+b);	
		
		}//while
		
	}//main

}//class
```

## x보다 작은 수

```jsx
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
	
		Scanner sc = new Scanner(System.in);
		
		int n = sc.nextInt(); //n개로 이루어진
		int x = sc.nextInt(); //x보다 작은 수 찾기
		int a[] = new int[n];
		
		for(int i = 0 ; i < n ; i++) {
			a[i] = sc.nextInt();
		if(x > a[i]) {
			System.out.print(a[i] + " ");
		}
		}//for

	}//main

}//class
```