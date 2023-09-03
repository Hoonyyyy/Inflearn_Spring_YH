# JPA 소개

# 지금 시대는 객체를 관계형 DB에 보관함

## SQL 개발에 문제점
- 무한 반복...
- CRUD

## 객체와 관계형 데이터베이스의 차이
- 상속
- 연관관계
- 데이터 타입
- 데이터 식별 방법

## 자바 컬렉션에서 저장하면???

## 계층형 아키텍처 진정한 의미의 계층 분할이 어렵다.
- 자바 컬렉션에서 조회에서 ==는 같다.

## 객체답게 모델링 할수록 매핑 작업만 늘어난다.

## 객체를 자바 컬렉션에 저장 하듯이 DB에 저장할 수는 없을까?

# JPA (Java Persistence API)
- ORM

## ORM
- 객체 관계 매핑
- 객체는 객체대로 설계
- 관계형 데이터베이스는 관계형 데이터베이스대로 설계
- ORM 프레임워크가 중간에서 매핑
- 대중적인 언어에는 대부분 ORM 기술이 존재
- JPA는 애플리케이션이랑 JDBC 사이에서 사용됨

## JPA는 표준 명세
- JPA는 인터페이스의 모음
- JPA 2.1 표준 명세를 구현한 3가지 구현체
- 하이버네이트, EclipseLink, DataNucleus
- 우리는 그냥  Hibernate 사용

## JPA를 왜 사용해야 하는가?
- SQL 중심적인 개발에서 객체 중심으로 개발
- 생산성
  - 저장 : jpa.persist(member)
  - 조회 : Member member = jpa.find(memberId)
  - 수정 : member.setName("변경할 이름")
  - 삭제 : jpa.remove(member)
- 유지보수
  - JPA : 필드만 추가하면 됨
- 패러다임의 불일치 해결
  - JPA와 상속
  - JPA와 연관관계, 객체 그래프 탐색
  - 신뢰할 수 있는 엔티티, 계층
  - JPA와 비교하기
    - 동일한 트랜잭션!!에서 가능
  - JPA 성능 최적화 기능
    - 1차 캐시와 동일성(identity) 보장
      - 같은 트랜잭션 안에서는 같은 엔티티를 반환 (약간의 조회 성능 향상)
      - DB Isolation Level이 Read Commit이어도 애플리케이션에서 Repeatable Read 보장
    - 트랜잭션을 지원하는 쓰기 지연(transaction write-behind)
      - 트랜잭션을 커밋할 때까지 INSERT SQL을 모음
      - JDBC BATCH SQL 기능을 사용해서 한번에 SQL 전송 (네트워크 연결 비용 줄어듬)
    - 지연 로딩(Lazy Loading)
      - 지연 로딩 : 객체가 실제 사용될 때 로딩
      - 즉시 로딩 : JOIN SQL로 한번에 연관된 객체까지 미리 조회
- 성능
- 데이터 접근 추상화와 벤더 독립성
- 표준








