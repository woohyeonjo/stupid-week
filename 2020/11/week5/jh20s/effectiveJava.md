53. 가변인수는 신중히 사용하라.
인수 개수가 일정하지 않은 메서드를 정의해야 한다면 가변인수가 반드시 필요하다.
메서드를 정의할때 필수 매개변수는 가변인수 앞에 두고, 가변인수를 사용할떄는 성능 문제까지 고려하자.

54. null이 아닌, 빈컬렉션이나 배열을 반환하라.
null이 아닌, 빈 배열이나 컬렉션을 반환하라.
null을 반환하는 api는 사용하기 어렵고 오류처리 코드도 늘어난다.
그렇다고 성능이 좋은 것도 아니다. -> 구글 aosp null반환 쥰나많던데

55. 옵셔널 반환은 신중히 하라
값을 반환하지 못할 가능성이 있고, 호출때마다 반환값이 없을 가능성을 염두에 둬야하는
메서드라면 옵셔널을 반환해야하 할 상황일 수 있다. 하지만 옵셔널 반환에는 성능 저하가 뒤따르니,
성능에 민감한 메서드라면 null을 반환하거나 예외를 던지는 편이 나을 수 있다.
그리고 옵셔널 반환값 이외의 용도로 쓰는 경우는 매우 드물다.

56. 공개된 api 요소에는 항상 문서화 주석을 작성하라
문서화 주석은 여러분 api를 문서화하는 가장 훌륭하고 효과적인 방법이다.
공개 api라면 빠짐없이 설명을 달아야한다. 표군 규약을 일관되게 지키자.
문서화주석에 임의 HTML태그를 사용할 수 있다.
단, html 메타문자는 특별하게 취급해야한다.