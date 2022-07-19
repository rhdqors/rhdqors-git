# while 을 이용한 간단한 학생점수 확인 프로그램


```jsx
public class Exercise {

		public static void main(String[] args) {

			boolean run = true;
			int studentNum = 0;
			int[] scores = null;
			Scanner sc = new Scanner(System.in);
			
			while(run) {
				System.out.println("_-------------------------------------------");
				System.out.println("1.학생수 | 2.점수입력 | 3.점수리스트| 4.분석 | 5.종료");
				System.out.println("_-------------------------------------------");
				System.out.println("선택> ");
			
				int selectNum = sc.nextInt();
				
				if( selectNum ==1 ) {
					System.out.println("학생수> ");
					studentNum = sc.nextInt();
					scores = new int[studentNum];
				}else if (selectNum ==2) {
					for(int i = 0; i < scores.length; i++) {
						System.out.println("scores[" + i + "]");
						scores[i] = sc.nextInt();
					}
				}else if (selectNum ==3) {
					for(int i = 0; i < scores.length; i++) {
						System.out.println("scores[" + i + "]");
				}
				}else if (selectNum ==4) {
					int max = 0;
					int sum = 0;
					double avg = 0;
					for(int i = 0; i < scores.length; i++) {
						max = (max<scores[i])?scores[i]:max;
								sum += scores[i];
					}
					avg = (double) sum / studentNum;
					System.out.println("최고 점수: " + max);
					System.out.println("평균점수: " + avg);
				}else if (selectNum ==5) {
				run = false;
					
					}//while
			
		}//main
			

		}
```