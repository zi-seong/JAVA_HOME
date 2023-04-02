# final과 effectively final

## final
- final 키워드는 엔티티를 한번만 할당한다. 두번 이상 할당하려 할 때 컴파일 오류가 발생함
- final 키워드는 클래스, 메소드, 변수에 사용할 수 있다.
- final class는 상속을 제한한다.
- final method는 오버라이드를 제한한다.
- final 이 변수에 사용되었을 때 primitive type이라면 상수값이 되고 reference type이라면 다른 참조 값(다른객체로)으로 변경 불가 대신 객체안에 있는 필드들은 변경 가능

## effectively final
- 자바 8에서 도입 되었고 final 키워드가 붙지 않았는데도 불구하고 값이 변경되지 않는 변수를 effective final이라고 한다.
- 자바 8이전에는 내부 클래스, 익명 클래스에서 외부 변수를 참조할 시 그 변수가 반드시 final 변수여야 했지만 effectively final 도입으로 final 키워드가 붙지 않은 변수라도 어디에서도 값이 변경되지 않는다면 final 변수처럼 내부 클래스, 익명 클래스, 람다 표현식에서 참조할 수 있게 되었음