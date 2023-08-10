# HTTP 메시지 컨버터

- 뷰 템플릿으로 HTML을 생성해서 응답하는 것이 아니라, HTTP API처럼 JSON 데이터를 HTTP 메시지 바디에서 직접 읽거나
- 쓰는 경우 HTTP 메시지 컨버터를 사용하면 편리하다.
- @ResponseBody의 사용원리는 pdf 그림으로 보기
- 응답의 경우 클라이언트이 HTTP Accept 헤더와 서버의 컨트롤러 반환 타입 정보 둘을 조합해서 HTTPMessageConverter가 선택됨

## 스프링 MVC의 HTTP 메시지 컨버터 적용 경우
- HTTP 요청 : @RequestBody, HttpEntity(RequestEntity),
- HTTP 응답 : @ResponseBody, HttpEntity(ResponseEntity)

## 주요 메시지 컨버터
- ByteArrayHttpMessageConverter : byte[] 데이터를 처리한다.
  - 클래스 타입: byte[] , 미디어타입: */* ,
  - 요청 예) @RequestBody byte[] data
  - 응답 예) @ResponseBody return byte[] 쓰기 미디어타입 application/octet-stream
- StringHttpMessageConverter : String 문자로 데이터를 처리한다.
  - 클래스 타입: String , 미디어타입: */*
  - 요청 예) @RequestBody String data
  - 응답 예) @ResponseBody return "ok" 쓰기 미디어타입 text/plain
- MappingJackson2HttpMessageConverter : application/json
  - 클래스 타입: 객체 또는 HashMap , 미디어타입 application/json 관련
  - 요청 예) @RequestBody HelloData data
  - 응답 예) @ResponseBody return helloData 쓰기 미디어타입 application/json 관련

