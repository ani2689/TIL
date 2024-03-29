### 제어의 역전

`IoC`란 `Inversion of Control`을 줄인 표현으로 직역하면 제어의 역적이 된다.

아래의 코드를 보자.

```java

public class A{
    B b = new B();
}

```

클래스 A가 클래스 B 객체를 사용하기 위해 클래스 A에서 객체를 직접 생성한다.

제어의 역전은 다른 객체를 직접 생성하거나 제어하는 것이 아닌 외부에서 관리하는 객체를 가져와 사용하는 것을 말한다.

제어의 역전을 적용하면 위의 코드는 이렇게 변하게 된다.

```java

public class A{
    private B b;
    
    public A(B b){
        this.b = b;
    }
}

```

클래스 A가 생성자를 통하여 객체 B를 받아온자. 이처럼 클래스 B 객체를 직접 생성하는 것이 아닌 어딘가에서 받아와 사용하면 제어의 역전이 적용되었다 라고 할 수 있다.

실제로 스프링은 스프링 컨테이너가 객체를 관리 및 제공하는 역할을 한다.