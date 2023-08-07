# HTTP 메서드 활용
- 클라이언트에서 서버로 데이터 전송
- HTTP API 설계 예시 


## 클라이언트에서 서버로 데이터 전송(데이터 전달 방식은 크게 2가지)
- 쿼리 파라미터를 통한 데이터 전송
  - GET
  - 주로 정렬 필터(검색어)
- 메시지 바디를 통한 데이터 전송
  - POST, PUT, PATCH
  - 회원가입, 상품주문, 리소스 등록, 리소스 변경

## 4가지 상황
- 정적 데이터 조회
  - 이미지, 정적 텍스트 문서
- 동적 데이터 조회
  - 주로 검색, 게시판 목록에서 정렬 필터(검색어)
- HTML Form을 통한 데이터 전송
  - 회원가입, 상품주문, 데이터 변경
- HTTP API를 통한 데이터 전송
  - 회원가입, 상품주문, 데이터 변경
  - 서버 to 서버, 앱 클라이언트, 웹 클라이언트(Ajax)

## 정적 데이터 조회
- 쿼리없이 조회가능

## 동적 데이터 조회 (쿼리 파라미터 사용)
- 검색, 게시판 목록 정렬 필터(검색어)
- 필터!필터!필터!, 조회는 GET 사용

(그다음 것들은 ppt로 보는게 나음)

- 참고 : HTML Form 전송은 GET,POST만 지원


### HTTP API 데이터 전송
- 서버 to 서버
  - 백엔드 시스템 통신
- 앱 클라이언트
  - 아이폰, 안드로이드
- 웹 클라이언트
  - HTML에서 Form 전송 대신 자바 스크립트를 통한 통신에 사용(AJAX)
  - 예) React, VueJS 같은 웹 클라이언트와 API 통신
- POST, PUT, PATCH : 메시지 바디를 통해 데이터 전송
- GET : 조회, 쿼리, 파라미터로 데이터 전달
- Content-Type : application/json을 주로 사용 (사실상 표준)
  - TEXT, XML, JSON 등등


# HTTP API 설계 예시
- HTTP API - 컬렉션
  - POST 기반 등록
  - 예) 회원 관리 API 제공
- HTTP API - 스토어
  - PUT 기반 등록
  - 예) 정적 컨텐츠 관리, 원격 파일 관리
- HTML FORM 사용
  - 웹 페이지 회원 관리
  - GET, POST만 사용

## 회원 관리 시스템
### POST - 신규 자원 등록 특징
- 클라이언트는 등록될 리소스의 URI를 모른다
  - 회원 등록/members -> POST
  - POST /members
- 서버가 새로 등록될 리소스 URI를 생성해준다.
  - HTTP/1.1 201 Create
  - Location : /members/100

- 컬렉션(Collection)
  - 서버가 관리하는 리소스 디렉토리
  - 서버가 리소스의 URI를 생성하고 관리
  - 여기서 컬렉션은 /members

## 파일 관리 시스템
### API 설계 - PUT 기반 등록
- 파일 목록 /files -> GET
- 파일 조회 /files/{filename} -> GET
- 파일 등록 /files/{filename} -> PUT
- 파일 삭제 /files/{filename} -> DELETE
- 파일 대량 등록 /files -> POST

### PUT - 신규 자원 등록 특징
- 클라이언트가 리소스 URI를 알고 있어야 한다.
  - 파일 등록 /files/{filename} -> PUT
  - PUT /files/star.jpg

- 클라이언트가 직접 리소스의 URI를 지정한다.
- 스토어(Store)
  - 클라이언트가 관리하는 리소스 저장소
  - 클라이언트가 리소스의 URI를 알고 관리
  - 여기서 스토어는 /files

















