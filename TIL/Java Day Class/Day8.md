## 인터페이스 활용



```
package thisisjava;

public interface DataAccessObject {

  public void select();

  public void insert();

  public void update();

  public void delete();

}
```



``` 
package thisisjava;
 class OracleDao implements DataAccessObject {

	@Override
	public void select() {
		System.out.println("Oracle Db에서 검색");
		
	}

	@Override
	public void insert() {
		System.out.println("Oracle Db에 삽입");
		
	}

	@Override
	public void update() {
		System.out.println("Oracle Db를 수정");
		
	}

	@Override
	public void delete() {
		System.out.println("Oracle Db에서 삭제");
		
	}
	
 }
 class MySqlDao implements DataAccessObject {

		@Override
		public void select() {
			System.out.println("MySql Db에서 검색");
			
		}

		@Override
		public void insert() {
			System.out.println("MySql Db에 삽입");
		
		}

		@Override
		public void update() {
			System.out.println("MySql Db를 수정");
			
		}

		@Override
		public void delete() {
			System.out.println("MySql Db에서 삭제");
			
		}
	}
	
public class DaoExample {
	public static void dbWork(DataAccessObject dao) {
	dao.select();
	dao.insert();
	dao.update();
	dao.delete();
	}//메소드
	
	public static void main(String[] args) {
		
		dbWork(new OracleDao());
		dbWork(new MySqlDao());
	
	}//main
}

```



---

Oracle Db에서 검색
Oracle Db에 삽입
Oracle Db를 수정
Oracle Db에서 삭제
MySql Db에서 검색
MySql Db에 삽입
MySql Db를 수정
MySql Db에서 삭제