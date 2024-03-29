대리자 (Delegate)의 정의
========================

C++에서의 함수(메서드)를 대신하는 대리자가 Delegate이다
Delegate는 대신할 메서드의 반환형과 매개변수가 동일해야 한다.

Delegate의 선언형식은 다음과 같다.
delegate 반환형 변수명 ( 매개변수명,..)

ex) delegate int customDelegate(int a, int b); 라는 델리게이트는

int ExFunc(int a, int b){<br>
  Debug.Log("이것은 함수입니다.");<br>
}<br>
이와 같이 같은 형식의 함수를 담을 수 있다.

Delegate에 사용할 수 있는 대표적인 문법에 '람다식, 무명메서드'라는 것이 있는데
무명메서드란 다시는 사용하지 않을만한 함수를 함수의 이름을 직접 선언하여 만들지 않고
컴파일러가 이름을 선언해주는 '이름없는 함수'로 만드는 것이고,
람다식이란 '=>' 연산자를 통해 코드를 간결하게 만들어준다. 
C# 3.0버전이상에서는 이 람다식의 사용을 권장한다고 한다.

예를 들어서 람다식은 유니티에서는 이벤트 핸들러에 많이 사용되고 있는데
button.onClick.AddListener(() => Func(0)); <br>
이것의 오른쪽 식을 람다식이라고 하고 
addListener의 함수는 기본적으로 매개변수가 없는 함수만 넣을 수 있기 때문에
무명메서드를 활용하여 인자가 있는 함수를 넣어준 방법이다.

기본적으로 제공하는 델리게이트들에는 3가지가 있는데 각각 예를 들어 간단하게 설명하겠다.
<h2>
  1. 반환형이 없는 경우(void인 경우) - Action<> </h2>
  Action은 <>에 들어가는 변수들이 모두 매개변수를 뜻한다.
  Action action;<br>
  action += () => { Debug.Log("무명 함수 입니다.")};<br>
  Action<int, int> action2;<br>
  void ExFunction(int a, int b){<br>
    Debug.Log("예제 함수입니다.");<br>
  }<br>
  action2 += ExFunction(1,2);<br>
<h2>
  2. 반환형이나 매개변수나 그 둘 다 있는 경우 - Func<></h2>
  <>안에 매개변수가 1개이면 매개변수만 있는 것이고 2개 이상이면 마지막이 반환형을 뜻한다.<br>
  Func<int>
  
<h2>
  3. 반환형이 bool형인 경우 - Predicate<T></h2>






