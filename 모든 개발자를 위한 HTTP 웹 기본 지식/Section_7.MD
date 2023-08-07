# HTTP 헤더1 - 일반 헤더

# HTTP 헤더
- HTTP 전송에 필요한 모든 부가정보
- 예) 메시지 바디의 내용, 바디의 크기, 압축 등등등...
- 표준 헤더가 너무 많음
- 필요시 임의 헤더 추가 가능
- RFC2616(과거)
  - General 헤더 : 메시지 전체에 적용되는 정보,  ex) Connection : close
  - Request 헤더 : 요청 정보, ex) User-Agent : Mozilla/5.0 (Macintosh; ..)
  - Response 헤더 : 응답 정보, ex) Server : Apache
  - Entity 헤더 : 엔티티 바디 정보, 예) Content-Type : text/html, Content-Length: 3424
  - HTTP BODY
    - 메시지 본문은 엔티티 본문을 저날하는데 사용
    - 엔티티 헤더는 엔티티 본문의 데이터를 해석할 수 있는 정보 제공

## 최신
- 메시지 본문을 통해 표현 데이터 전달
- 메시지 본문 = 페이로드(payload)
- 표현은 요청이나 응답에서 전달할 실제 데이터
- 표현 헤더는 표현 데이터를 해석할 수 있는 정보 제공
  - 데이터 유형(html, json), 데이터 길이, 압축 정보 등등

## 표현
- Content-Type : 표현 데이터의 형식
- Content-Encoding : 표현 데이터의 압축 방식
- Content-Language : 표현 데이터의 자연 언어
- Content-Length : 표현 데이터의 길이
- 표현 헤더는 전송, 응답 둘다 사용

### Content-Type (표현 데이터의 형식 설명)
- 미디어 타입, 문자 인코딩
- ex) text/html; ~, applcation/json(얘가 기본 UTF-8), image/png

### Content-Encoding (표현 데이터 인코딩)
- 표현 데이터를 압축하기 위해 사용
- 데이터를 전달하는 곳에서 압축 후 인코딩 헤더 추가
- 데이터를 읽는 쪽에서 인코딩 헤더의 정보로 압축 해제
- ex) gzip, deflate, identity

### Content-Language (표현 데이터의 자연 언어)
- 표현 데이터의 자연 언어를 표현
- 예) ko, en, en-US

### Content-Length (표현 데이터의 길이)
- 바이트 단위
- Transfer-Encoding(전송 코딩)을 사용하면 Content-Length 사용하면 안됨

## 협상(콘텐츠 네고시에이션)(클라이언트가 선호하는 표현 요청)
- 협상 헤더는 요청시에만 사용
  - Accept : 클라이언트가 선호하는 미디어 타입 전달
  - Accept-Charset : 클라이언트가 선호하는 문자 인코딩
  - Accept-Encoding : 클라이언트가 선호하는 압축 인코딩
  - Accept-Language : 클라이언트가 선호하는 자연 언어




























