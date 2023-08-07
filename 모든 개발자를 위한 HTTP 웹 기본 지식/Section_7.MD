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

### 협상과 우선순위1 ( Quality Values(q) )
- Quality Values(q) 값 사용
- 0~1, 클수록 높은 우선순위
- 생략하면 1
- Accept-Language : ko-KR,ko;q=0.9,en-US;q=0.8,en;q=0.7
  - 1. ko-KR;q=1 (q생략)
  - 2. ko;q=0.9
  - 3. en-US;q=0.8
  - 4. en:q=0.7

### 협상과 우선순위2 ( Quality Values(q) )
- 구체적인 것이 우선한다!!!
- Accept: text/*, text/plain, text/plain;format=flowed, */*
  - text/plain;format-flowed
  - text/plain
  - text/*
  - */*

### 협상과 우선순위3 ( Quality Values(q) )
- 구체적인 것을 기준으로 미디어 타입을 맞춘다.
- 보통 여기까지는 안옴



## 전송 방식
- 단순 전송
- 압축 전송
- 분할 전송
- 범위 전송

### 단순 전송
- Content-Length

### 압축 전송
- Content-Length
- 절반 이상 줄어드는 경우가 많음

### 분할 전송
- Transfer-Encoding
- Content-Length 넣으면 안됨! 예상이 안됨

### 범위 전송
- Range, Content-Range

## 일반 정보

### From (유저 에이전트 이메일 정보)
- 잘 사용 안함
- 검색 엔진 같은 곳에서, 주로 사용

### Referer (이전 웹 페이지 주소)
- 현재 요청된 페이지 이전 주소
- Referer를 사용해서 유입 경로 분석 가능
- 참고 : referer는 단어 referrer의 오타

### User-Agent (유저 에이전트 애플리케이션 정보)
- 통계 정보
- 클라이언트의 애플리케이션 정보

### Server (요청을 처리하는 ORIGIN 서버의 소프트웨어 정보)
- Server: Apache/2.2.22 (Debian)
- server : nginx
- 응답에서 사용

### Date(메시지가 발생한 날짜와 시간)
- 응답에서 사용

## 특별한 정보

### Host( 요청한 호스트정보(도메인) )
- 요청에서 사용
- 필수
- 하나의 서버가 여러 도메인을 처리해야 할 때

### Location (페이지 리다이렉션)
- 웹 브라우저는 3xx 응답의 결과에 Location 헤더가 있으면, Location 위치로 자동 이동(리다이렉트)
- 응답코드 3xx에서 설명
- 201 (Created) : Location 값은 요청에 의해 생성된 리소스 URI
- 3xx (Redirection) : Location 값은 요청을 자동으로 리다이렉션하기 위한 대상 리소스를 가리킴

### Allow (허용 가능한 HTTP 메서드)
- 405(Method Not Allowed)에서 응답에 포함해야함
- Allow: GET, HEAD, PUT
- 서버에서 별로 구현되어 있지 않음

### Retry-After (유저 에이전트가 다음 요청을 하기까지 기다려야 하는 시간)
- 503(Service Unavailable) : 서비스가 언제까지 불능인지 알려줄 수 있음
- 사용하기 쉽지않음

## 인증

### Authorization (클라이언트 인증 정보를 서버에 전달)

### WWW_Authenticate (리소스 접근시 필요한 인증 방법 정의)

# 쿠키



















