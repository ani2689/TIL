# HTTP Response

HTTP 요청과 구조는 비슷하다.

## Status Line

응답에서의 중요한 내용이 담긴다.

### HTTP Version 

HTTP의 버전 정보가 담긴다.

### Status Code

응답에서 가장 중요한 상태 코드 값이다. 

### Status Text

상태 코드와 함께 상태를 설명하는 텍스트가 뒤에 붙기도 한다. 

## Headers

헤더에서 제일 중요한 것인 메세지 바디가 어떤 컨텐츠 타입으로 작성되어 있는지의 정보가 들어있다.

그 외의 서버가 클라이언트에게 보내주고 싶은 정보들이 헤더에 추가될 수 있다.

## Message Body

GET 같은 메서드는 메세지 바디가 동반되며, 그 정보가 담긴다.  