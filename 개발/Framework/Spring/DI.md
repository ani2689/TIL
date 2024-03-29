### 의존성 주입

`Dependency Injection`, 의존성 주입이란 어떤 클래스가 다른 클래스에 의존한다는 뜻이다.

- 다양한 의존 관계 주입 방법
    - 생성자 주입
        - 생성자 메서드에 @Autowired를 붙인다.
        - 장점
            - final을 선언 할 수 있어 의존성이 변할 걱정을 하지 않아도 된다.
            - null오류가 발생하지 않는다.
            - 필수적으로 사용해야하는 의존성을 추가하지 않으면 객체를 만들 수 없도록 강제한다.
    - 수정자(Setter) 주입
        - setter 메서드에 @Autowired를 붙인다.
        - 장점
            - 선택적인 의존성을 사용할 때 편리하다.
        - 단점
            - 주입이 필요한 객체가 얼마든지 생성 될 수 있다.
    - 필드 주입
        - 변수 선언 부에 @Autowired를 붙인다.
        - 장점
            - 붙이기만 하면 돼서 간단하다.
        - 단점
            - final을 선언 할 수 없어 객체가 변할 수 있다.
            - 순수한 자바 테스트 코드로 작동 시킬 수 없다.
