# Bank account
import java.util.Scanner;

class Account {
   
   private String ano;
   private String owner;
   private int balance;
   
   public Account( String ano, String owner, int balance ) {
      this.ano = ano;
      this.owner = owner;
      this.balance = balance;
   }

   public String getAno()  {return ano;}

   public void setAno(String ano) {this.ano = ano;}

   public String getOwner() {return owner;}

   public void setOwner(String owner) {this.owner = owner;}

   public int getBalance() {return balance;}

   public void setBalance(int balance) {this.balance = balance;}
   
}//class


public class BankApplication {

	 private static Account[] accountArray = new Account [100];
     private static Scanner scanner = new Scanner(System.in);
     
   public static void main(String[] args) {
     
	   
	   boolean run = true;
     while(run) {
    	 System.out.println("----------------------------------------");
    	 System.out.println("1.계좌생성 | 2.계좌목록 | 3.예금 | 4.출금 | 5.종료");
    	 System.out.println("----------------------------------------");
    	 System.out.print("선택> ");
     
    	 int selectNum = scanner.nextInt();
    	 
    	 if( selectNum == 1 ) {
    		 createAccount();
    	 }else if (selectNum == 2) {
    		 accountList();
    	 }else if (selectNum == 3) {
    		 deposit();
    	 }else if (selectNum == 4) {
    		 withdraw();
    	 }else if (selectNum == 5) {
    		 run = false;
    	 }//if
    	 
    	 }//while
     System.out.println("프로그램 종료");
   }//main
     
   private static void createAccount() {
	   System.out.println("--------");
	   System.out.println("계좌생성");
	   System.out.println("--------");
	   System.out.print("계좌번호: ");
	   String ano =  scanner.next();
	   System.out.print("계좌주: ");
	   String owner = scanner.next();
	   System.out.print("초기입금액: ");
	   int balance = scanner.nextInt();
 	  
 	  Account newAccount = new Account(ano, owner, balance);
 	  
 	  	for (int i = 0 ; i <accountArray.length ; i++ ) {
 	  		if (accountArray [i]== null) { 
 	  		   accountArray[i] = newAccount;
 	  		System.out.println("결과: 계좌가 생성되었습니다.");
 	  		break;
 	  		}//if
 	  	}//for
   }//create
   
   private static void accountList() {
	   System.out.println("--------");
	   System.out.println("계좌목록");
	   System.out.println("--------");
		
	   for (int i = 0 ; i <accountArray.length ; i++ ) {
	   Account account = accountArray[i];
			if ( account != null ) {
		   System.out.print(account.getAno());
		   System.out.print("     ");
		   System.out.print(account.getOwner());
		   System.out.print("     ");
		   System.out.print(account.getBalance());
		   System.out.println("     ");
	   }//if
	}//for
   }//List
   
   private static void deposit () {
	   
	   System.out.println("--------");
	   System.out.println("예금");
	   System.out.println("--------");
	   System.out.print("계좌번호: ");
	   String ano =  scanner.next();
	   System.out.print("예금액: ");
	   int money = scanner.nextInt();
	   
	   Account account = findAccount(ano);
	   
	   System.out.println("예금이 성공되었습니다.");
   }
   
   private static Account findAccount(String ano) {
	Account account = null;
	for(int i = 0 ; i < accountArray.length ; i++) {
		if ( accountArray[i] !=null ) { 
			String dbAno = accountArray[i].getAno();
			if (dbAno.equals(ano)) {
				account = accountArray[i];
				break;
			}
		}
	}
	return null;
}

private static void withdraw () {
	   System.out.println("--------");
	   System.out.println("출금");
	   System.out.println("--------");
	   String [] tmp = {"계좌번호: ", "출금액: "};
	   for (int i = 0 ; i < tmp.length ; i++ ) {
		   System.out.println(tmp[i]);
		   scanner.next();
	   }//for
	   System.out.println("출금이 성공되었습니다.");
	 // System.exit(0);
   }
   
   
}//BankApplication class
