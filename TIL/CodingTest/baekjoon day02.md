## 백준 주사위 세개

```jsx
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
	
		Scanner sc = new Scanner(System.in);
		
		int max = 0;
		int a = sc.nextInt();
		int b = sc.nextInt();
		int c = sc.nextInt();
		int arr1[] = {a, b, c};
		
		if (a == b && b == c && a == c) {
			System.out.println(10000 + a * 1000);
		}else if (a == b) {
			System.out.println(1000 + a * 100);
			
		}else if (a == c) {
			System.out.println(1000 + c * 100);
			
		}else if (b == c) {
			System.out.println(1000 + b * 100);
			
		}else if (a != b && b != c && a != c) {
			for(int i = 0 ; i < arr1.length ; i++) {
				if(arr1[i] > max) {
					max =arr1[i];	
				}//for if
			}System.out.println(max * 100);
			
		}
	
	}//main

}//class
```

## 백준 알람시계 문제(45분 일찍 알람 설정하기)

```jsx
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
	
		Scanner sc = new Scanner(System.in);
	
		int h = sc.nextInt();
		int m = sc.nextInt();
			//System.out.println(h + " " + m);
		if (m < 45 && h == 0) {
			h = 23;
			System.out.println(h + " " + (m+(60-45)));
		}else if (m >= 45) {
			System.out.println(h + " " + (m-45));
		}else if (m < 45) {
			h--;
			System.out.println(h + " " + (60-(45-m)));
		}
	
	}//main

}//class
```
