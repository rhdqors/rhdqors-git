# HTML을 이용한  게시물 리스트 조회

```jsx
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
</head>
<body>

<h1>환영합니다</h1>
<ul>
<li><a href="boardlist.html">게시물리스트</a></li>
<li><a href="boardwrite.html">글쓰기</a></li>
<li><a href="#">회원가입</a></li>
<li><a href="#">로그인</a></li>
</ul>

</body>
</html>
```

```jsx
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
</head>
<body>
<h1>boardlist를 출력합니다.</h1>
<form action="boardsearch.html">
<select name="list">
<option>제목</option>
<option>내용</option>
<option>작성자</option>
</select>
검색어:<input type="text" name="search"> <input type="submit" value="검색">
<br>
<br>
<div style="border:2px solid aqua">
<table border="2">
<tr><td>번호</td><td>제목</td><td>작성자</td><td>조회수</td></tr>
<tr><td>1</td><td><a href="boarddetail.html">제목1</a></td><td>작성자1</td><td>0</td></tr>
<tr><td>2</td><td><a href="boarddetail.html">제목2</a></td><td>작성자2</td><td>0</td></tr>
<tr><td>3</td><td><a href="boarddetail.html">제목3</a></td><td>작성자3</td><td>11</td></tr>
<tr><td>4</td><td><a href="boarddetail.html">제목4</a></td><td>작성자4</td><td>22</td></tr>
<tr><td>5</td><td><a href="boarddetail.html">제목5</a></td><td>작성자5</td><td>11</td></tr>
</table>
</div>
<p>
<h4>페이지번호</h4>
</p>

<a href="#">1</a>   
<a href="#">2</a>   
<a href="#">3</a>   
<a href="#">4</a>   
<a href="#">5</a>
</form>

</body>
</html>
```