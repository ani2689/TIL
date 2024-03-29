# Proxy 

Decorator와 유사한 구조. 객체지향 디자인 패턴에 나오는 패턴 중 하나이다.

프록시 객체는 언뜻 인터페이스를 구현한 객체처럼 보이지만 실제로는 이것을 대리하여 부가적인 효과를 제공한다.

## Lazy Loading

실제 로직을 가지고 있는 구현 객체가 굉장히 크고 비싸다. 만드는데 메모리도 시간도 많이드는 객체인 것이다. 

서버를 시작할 때 굳이 미리 다 만들어 둘 필요 없이 어떠다 호출될 때, 첫 번째 요청이 들어오면 그때 객체를 만들어야 되는, 최대한 지연시켜서 얘를 가져와야 하는 객체가 있을 때 프록시 패턴을 사용할 수 있다.

## Remote Access

로컬에 인터페이스를 구현하는 객체가 있다고 생각했으나 사실은 API를 타고 네트워크 넘어 멀리 있는 어떤 서버에 존재하는 객체를 사용해야 하는 경우가 있다.  

이때 프록시가 API 호출을 하여 원격에 있는 객체를 수행시켜 그 결과를 받아 반환한다. 이러면 실행자는 자신이 지금 원격에 있는 객체를 호출하는지, 아직 존재하지 않았지만 최초 요청을 보냈을 때 객체가 생성되어 그 애로부터 결과를 받아오는지에 대해서는 전혀 신경쓰지 않게 해주며 둘 중 하나가 변경되더라도 영향을 받지 않도록 프록시가 그 중간에서 대리자 역할을 한다.

## Other

그 외에도 이걸 사용하는 어떤 보안 기능을 적용한다거나 액세스 컨트롤 하는 등의 기능 등을 적용해 볼 수 있다.

JPA나 Spring 애플리케이션에서도 프록시 패턴을 사용한다.
