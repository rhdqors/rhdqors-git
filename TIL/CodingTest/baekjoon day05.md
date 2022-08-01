![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ba3460c7-4a1d-43d6-846c-7d56e77a90c4/Untitled.png)

## 더하기 사이클

```jsx
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class Main {

	public static void main(String[] args) throws Exception {
	
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));  
		int n = Integer.parseInt(br.readLine());
		
		int a = 0; //10의자리
		int b = 0;  //1의자리
		int nn = n;
		int cycle = 0;
		
		while (true) {
			 cycle++;
			 a = nn/10;
			 b = nn%10;
			nn =  b * 10 + (a + b) % 10;
		if (n == nn) {
			break;
			}
		}
		
		System.out.println(cycle);
		
	}//main

}//class
```