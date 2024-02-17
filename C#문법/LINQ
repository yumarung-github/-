LINQ와 SQL 기본 문법 

	var Customers = db.GetTable<Customers>();
	var custumQuery = from cust in customers
			  where cust.City == “London”
			  select cust;
foreach (var item in custQuery) {
	console.writeLine(item);
}

쿼리문을 GetTable을 통해 가져와서 쿼리문으로 사용하기

var변수를 이용해서 쿼리문을 저장하면 쿼리문에서 from절에서 지정된 데이터소스를 확인하여
쿼리 변수의 형식을 유추하도록 컴파일러에 지시하여 제네릭형식을 사용하지 않아도 됨.
