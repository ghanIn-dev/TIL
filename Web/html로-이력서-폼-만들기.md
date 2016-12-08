# HTML로 이력서 폼 만들기

* html5 에서부터는`width=10%` 형식의 태그를 지원하지 않음 -&gt; `style="width=10%;"` 의 형태로 사용해야 함  링크

* rowspan과 colspan의 수가 변함\(아래또는 위 행의 영향으로\)

* width percent가 작동하지 않아 검색해본 결과 `table-layout: fixed;` 을 style 태그에 넣으니 정상작동됨 [링크 ](http://www.homejjang.com/09/table_layout.php) [링크](http://stackoverflow.com/questions/27587620/cant-change-table-cell-width)

* ```
   table-layout: fixed; 

   table-layout 속성값을 fixed로 지정하면 셀안의 데이터가 길어서 지정한 너비 이상으로 셀을 밀어버리는 것을 방지합니다.
  보통 셀안의 내용이 한글인 경우 공백이 중간 중간에 들어가므로 자동으로 지정한 너비에서 줄바꿈이 일어납니다.
  ```

* 원하는 부분 bold 처리    [링크](http://stackoverflow.com/questions/6379930/how-we-can-bold-only-the-name-in-table-td-tag-not-the-value) 
  `<span style="font-weight:bold">이력서</span>`

* 아래 그림은 만들려 참고했던 이력 양식이다.
  ![](/assets/기본_이력서_양식_2001.jpg)


```

<!DOCTYPE html>

<html>

<head>

<meta charset="EUC-KR">

<style type="text/css">

table {

 text-align: center;

 table-layout: fixed;

}

</style>

<title>Insert title here</title>

</head>

<body>

 <table border="1" style="width: 100%;" align="center">

 <tr>

 <td rowspan="4" style="width: 20%" colspan="3">사진</td>

 <td colspan="4" style="width: 70%">이력서</td>

 </tr>

 <tr>

 <td style="width: 20%" rowspan="2">성명</td>

 <td rowspan="2">인</td>

 <td colspan="2">주민등록번호</td>

 <tr>

 <td style="width: 30%" colspan="2">&nbsp; &nbsp;</td>

 </tr>

 </tr>

 <tr>

 <td style="width: 30%">생년월일</td>

 <td style="width: 100%" colspan="3">&nbsp; &nbsp; &nbsp; &nbsp;년

 &nbsp; &nbsp;&nbsp; &nbsp;월 &nbsp; &nbsp;&nbsp; &nbsp;일생(만 &nbsp;

 &nbsp;세)</td>

 </tr>

 <tr>

 <td style="width: 30%" colspan="3">주소</td>

 <td style="width: 100%" colspan="4"></td>

 </tr>

 <tr>

 <td style="width: 30%" rowspan="2" colspan="3">연락처</td>

 <td>집</td>

 <td></td>

 <td style="width: 30%" rowspan="2">전자우편</td>

 <td style="width: 30%" rowspan="2"></td>

 </tr>

 <tr>

 <td style="width: 30%">휴대폰</td>

 <td style="width: 30%"></td>

 </tr>

 <tr>

 <td style="width: 30%" colspan="3">호적 관계</td>

 <td style="width: 20%">호주와의 관계</td>

 <td style="width: 30%"></td>

 <td style="width: 30%">호주 성명</td>

 <td style="width: 30%"></td>

 </tr>

 <tr>

 <td style="width: 30%" colspan="3">년 월 일</td>

 <td style="width: 50%" colspan="2">학력 및 경력 사항</td>

 <td style="width: 30%" colspan="2">비고</td>

 </tr>

 <tr>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 </tr>

 <tr>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 </tr>

 <tr>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 </tr>

 <tr>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 </tr>

 <tr>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 </tr>

 <tr>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 </tr>

 <tr>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 </tr>

 <tr>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 </tr>

 <tr>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td>&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 <td colspan="2">&nbsp; &nbsp;</td>

 </tr>

 </table>

</body>

</html>

```

