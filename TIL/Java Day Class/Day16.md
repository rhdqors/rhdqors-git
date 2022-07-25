# html - 상품 등록 페이지
```jsx
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
</head>
<body>

<form action="html5.jsp">
색상선택 : <input type="color" name="col"><br>
날짜선택 : <input type="date" name="da"><br>
이메일 : <input type="email" name="em"><br>
홈페이지 : <input type="url" name="ur"><br>
연락처 : <input type="tel" name="te"><br>
숫자 : <input type="number" step="5" min="20" max="100" name="nu"><br>
범위 : <input type="range" name="ra"><br>
<input type="submit" value="버튼이름">
</form>

<hr>

<form action="produck.jsp">
<table border="1">
<tr><td colspan="2"><d>상품등록화면</d></td></tr>
<tr><td colspan="2">html5<img src="images/html5.jpg" width="50" height="50">를 이용한 상품 등록 페이지 입니다.</td></tr>
<tr><td>상품코드</td><td><input type="text" name="co" maxlength="10"></td></tr>
<tr><td>상품명</td><td><input type="text" name="na" maxlength="100"></td></tr>
<tr><td>가격</td><td><input type="radio" name="price" value="1000">1000
<input type="radio" name="price" value="2000">2000
<input type="radio" name="price" value="3000">3000
<input type="radio" name="price" value="4000">4000</td></tr>
<tr><td>재고수량</td><td><input type="number" step="2" min="1" max="50" name="nu"></td></tr>
<tr><td>분류</td><td><input type="checkbox" name="stock" value="electric">가전
<input type="checkbox" name="stock" value="cloth">의류
<input type="checkbox" name="stock" value="food">식품
<input type="checkbox" name="stock" value="fcs">의식주</td></tr>
<tr><td><input type="submit" value="상품등록"></td></tr>

</table>
</form>

</body>
</html>
```