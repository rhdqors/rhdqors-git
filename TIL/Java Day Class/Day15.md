# MYSQL 연동 데이터 삽입/조회 프로그램

```jsx
package javaExam1;

public class BookDTO extends BookTest {
	String bookNo;
	String bookTitle;
	String bookAuthor;
	String bookYear;
	int bookPrice;
	String bookPublisher;
	
	public String getBookNo() {
		return bookNo;
	}
	public void setBookNo(String bookNo) {
		this.bookNo = bookNo;
	}
	public String getBookTitle() {
		return bookTitle;
	}
	public void setBookTitle(String bookTitle) {
		this.bookTitle = bookTitle;
	}
	public String getBookAuthor() {
		return bookAuthor;
	}
	public void setBookAuthor(String bookAuthor) {
		this.bookAuthor = bookAuthor;
	}
	public String getBookYear() {
		return bookYear;
	}
	public void setBookYear(String bookYear) {
		this.bookYear = bookYear;
	}
	public int getBookPrice() {
		return bookPrice;
	}
	public void setBookPrice(int bookPrice) {
		this.bookPrice = bookPrice;
	}
	public String getBookPublisher() {
		return bookPublisher;
	}
	public void setBookPublisher(String bookPublisher) {
		this.bookPublisher = bookPublisher;
	}

	@Override
	public String toString() {
		return "도서 번호=" + bookNo + ",도서 제목=" + bookTitle + ",저자=" + bookAuthor + ",발행연도=" + bookYear
				+ ",가격=" + bookPrice + ",출판사=" + bookPublisher;
	}//toString

	
	
}//class
```

```jsx
package javaExam1;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;

public class BookDAO extends BookTest {

	public void insertBook( ) { // book 테이블에 데이터 저장

		Connection con = null;
		
		try {
		Class.forName("com.mysql.cj.jdbc.Driver");
		//System.out.println("호출 완료");
		con = DriverManager.getConnection("jdbc:mysql://127.0.0.1:3306/empdb", 
				"emp", "emp");
		
		String sql = " insert into book "
				+ " values( 'B004', 'HTML/CSS', '고길동', '2021-01-01'. 38000, '서울출판사)";
		Statement st = con.prepareStatement(sql);
		System.out.println("insert 완료");
		
		
		}catch (ClassNotFoundException e) {
			System.out.println("드라이버 호출 실패");
		}catch(SQLException e) {
			System.out.println("db연결(경로) 실패");
			e.printStackTrace();
		}finally {
			try {
			con.close();
			}catch(SQLException e) {}
		}
	}//insertbook
	
	public void selectBook() {//book 테이블에 있는 모든 데이터 출력
		
		Connection con = null;
		
		try {
		Class.forName("com.mysql.cj.jdbc.Driver");
		//System.out.println("호출 완료");
		con = DriverManager.getConnection("jdbc:mysql://127.0.0.1:3306/empdb", 
				"emp", "emp");
		//System.out.println("db연결 완료");
		
		String query = "select * from book";
		Statement st = con.createStatement(); //(현재는 비어있는) sql저장 가능한 객체 생성
		ResultSet rs = st.executeQuery(query);
		while(rs.next()) {//1번레코드이동
			System.out.println(rs.getString(1)+ "		" + rs.getString(2) + " 	" + rs.getString(3) + "	" 
		+ rs.getString(4) + "	" + rs.getString(5) + "	" + rs.getString(6));
		}
		
		rs.close();
		
		}catch (ClassNotFoundException e) {
			System.out.println("드라이버 호출 실패");
		}catch(SQLException e) {
			System.out.println("db연결(경로) 실패");
		}finally {
			try {
			con.close();
			}catch(SQLException e) {}
		}

	}//selectbook

}//class
```

```jsx
package javaExam1;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;
import java.util.Scanner;

import dao.MemberDAO;
import dto.MemberDTO;

public class BookTest {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		BookDAO dao = new BookDAO();
		Connection con = null;
		boolean run = true;
		
		try {
		Class.forName("com.mysql.cj.jdbc.Driver");
		//System.out.println("호출 완료");
		con = DriverManager.getConnection("jdbc:mysql://127.0.0.1:3306/empdb", 
				"emp", "emp");
		//System.out.println("db연결 완료");
		while(run) {
		System.out.println("=============================");
		System.out.println("1. book 테이블에 데이터 저장");
		System.out.println("2. book 테이블의 모든 데이터 출력");
		System.out.println("3. 종료");
		System.out.println("=============================");
		System.out.print("선택 >");
		int menu = sc.nextInt();
		if(menu == 1) {
		dao.insertBook();
		}else if (menu == 2) {
		dao.selectBook();
		}else if (menu == 3) {
			System.out.println("프로그램 종료합니다.");
			run = false;
		}
		}//while
		
		}catch (ClassNotFoundException e) {
			System.out.println("드라이버 호출 실패");
			e.printStackTrace();
		}catch(SQLException e) {
			System.out.println("db연결(경로) 실패");
			e.printStackTrace();
		}finally {
			//4. 연결해제
			try {
			con.close() ;//l 외부 연결 허용 최대치 - 100여개
			System.out.println("연결 해제 성공");
			}catch(SQLException e) { }
		}
		
	}//main

}//class
```