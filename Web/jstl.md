# &lt;c:foreach&gt;

일반적으로 특별하게 사용할 속성이 없다면 var와 items만 이용하여 아래와 같이 사용할 수 있다.

&lt;c:forEach var="item" items="${list}"&gt;

이름 : ${item.name}

나이 : ${item.age}

주소 : ${item.addr}

&lt;\/c:forEach&gt;

