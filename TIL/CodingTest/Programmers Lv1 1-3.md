## 윷놀이
```jsx
	public static void main(String[] args) {
	
		for(int i = 1; i < 4; i++) {
			int num1 =(int)(Math.random()*2);
			int num2 =(int)(Math.random()*2);
			int num3 =(int)(Math.random()*2);
			int num4 =(int)(Math.random()*2);
			
			int sum = num1 + num2 + num3 + num4;
			String number = num1 + "," + num2 + "," + num3 + "," + num4;
			
			if(sum == 3){
				System.out.println(number + " 도");
			}else if (sum == 2) {
				System.out.println(number + " 개");
			}else if (sum == 1) {
				System.out.println(number + " 걸");
			}else if (sum == 0) {
				System.out.println(number + " 윷");
			}else if (sum == 4) {
				System.out.println(number + " 모");
			}//if
		}//for
	
	}//main
}//class
```
---
## 행렬의 덧셈
```jsx
class Solution {
    public int[][] solution(int[][] arr1, int[][] arr2) {
      
        int[][] answer = new int[arr1.length][arr1[0].length];
	       
        for(int i = 0; i < arr1.length; i++ ){
	        	for(int k = 0; k < arr1[0].length; k++) {
	        	answer[i][k] = arr1[i][k] + arr2[i][k];
	        	
             }//innerfor
	        }//outfor
          return answer;
    
    }
}
```
---
## x만큼 간격이 있는 n개의 숫자
```jsx
class Solution {
    public long[] solution(int x, int n) {
      long[] answer = new long[n];
        
        for(int i = 0; i < answer.length;i++){
        answer[i] = (long)x*(i+1);
        
        }
        return answer;
}
}
```
---
## 직사각형 별찍기
```jsx
import java.util.Scanner;

class Solution {
    public static void main(String[] args) {
   Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        
        for(int k = 1; k <= b; k++) {
			for(int j = 1; j <= a; j++) {
				System.out.print("*");
			}System.out.println();
		}
      
        
    }
}
```