# 메소드 복습



class Computer{
	

	public int sum1 (int[] values) {
	int sum = 0;
	for( int i = 0 ; i < values.length; i++ ) {
		sum+= values[i];
	}
	return sum;
	}
	}//class





public class ComputerEx {

	public static void main(String[] args) {
		
		Computer c1 = new Computer();
		int values[] = { 1,2,3,4,5,6 };
		int result = c1.sum1(values);
		System.out.println(result);
		}//main
		}//class


​	





