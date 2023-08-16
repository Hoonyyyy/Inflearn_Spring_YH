# 김영한님 Java spring

## 실행 전 해야 할것
- IntelliJ settings에서 Annotation 체크
- gradle(intellij, intellij 바꾸기)
- Directory Mappings -
```
ion$DefaultTemplateResolverConfiguration

이 warn template에 index.html 하나 만들기
```

## 톰캣 서버 종료(맥)
```
sudo lsof -i :8080
 
kill -9 [PID number]
```

# 입문편
- [스프링 입문](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%94%84%EB%A7%81%EA%B3%B5%EB%B6%80/%EC%8A%A4%ED%94%84%EB%A7%81%EC%9E%85%EB%AC%B8.md#start)


# 스프링 핵심원리 기본편
## section1
- [스프링 생태계](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20%ED%95%B5%EC%8B%AC%20%EC%9B%90%EB%A6%AC%20-%20%EA%B8%B0%EB%B3%B8%ED%8E%B8/%EC%8A%A4%ED%94%84%EB%A7%81%20%EC%83%9D%ED%83%9C%EA%B3%84.MD#%EC%8A%A4%ED%94%84%EB%A7%81-%EC%83%9D%ED%83%9C%EA%B2%8Cmd)
- [좋은 객체지향 프로그램](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20%ED%95%B5%EC%8B%AC%20%EC%9B%90%EB%A6%AC%20-%20%EA%B8%B0%EB%B3%B8%ED%8E%B8/%EC%A2%8B%EC%9D%80%20%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5%20%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%A8.MD#%EC%A2%8B%EC%9D%80-%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%A8)
- [좋은 객체지향 원칙](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20%ED%95%B5%EC%8B%AC%20%EC%9B%90%EB%A6%AC%20-%20%EA%B8%B0%EB%B3%B8%ED%8E%B8/%EC%A2%8B%EC%9D%80%20%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5%EC%9D%98%20%EC%9B%90%EC%B9%99(SOLID).MD#%EC%A2%8B%EC%9D%80-%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5%EC%9D%98-%EC%9B%90%EC%B9%99solid)
- [객체 지향 설계와 스프링](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20%ED%95%B5%EC%8B%AC%20%EC%9B%90%EB%A6%AC%20-%20%EA%B8%B0%EB%B3%B8%ED%8E%B8/%EA%B0%9D%EC%B2%B4%20%EC%A7%80%ED%96%A5%20%EC%84%A4%EA%B3%84%EC%99%80%20%EC%8A%A4%ED%94%84%EB%A7%81.MD#%EA%B0%9D%EC%B2%B4-%EC%A7%80%ED%96%A5-%EC%84%A4%EA%B3%84%EC%99%80-%EC%8A%A4%ED%94%84%EB%A7%81)

## section2
- 코드로 작성해둠

# 모든 개발자를 위한 HTTP 웹 기본 지식
- [Section_1, ip dns 등](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EB%AA%A8%EB%93%A0%20%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%A5%BC%20%EC%9C%84%ED%95%9C%20HTTP%20%EC%9B%B9%20%EA%B8%B0%EB%B3%B8%20%EC%A7%80%EC%8B%9D/Section_1.MD#section_1)
- [Section_2, URI](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EB%AA%A8%EB%93%A0%20%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%A5%BC%20%EC%9C%84%ED%95%9C%20HTTP%20%EC%9B%B9%20%EA%B8%B0%EB%B3%B8%20%EC%A7%80%EC%8B%9D/Section_2.MD#section_2)
- [Section_3, HTTP](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EB%AA%A8%EB%93%A0%20%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%A5%BC%20%EC%9C%84%ED%95%9C%20HTTP%20%EC%9B%B9%20%EA%B8%B0%EB%B3%B8%20%EC%A7%80%EC%8B%9D/Section_3.MD#http-%EA%B8%B0%EB%B3%B8)
- [Section_4, HTTP 메서드](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EB%AA%A8%EB%93%A0%20%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%A5%BC%20%EC%9C%84%ED%95%9C%20HTTP%20%EC%9B%B9%20%EA%B8%B0%EB%B3%B8%20%EC%A7%80%EC%8B%9D/Section_4.MD#section_4)
- [Section_5, HTTP 메서드 활용 HTTP API 설계 예시](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EB%AA%A8%EB%93%A0%20%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%A5%BC%20%EC%9C%84%ED%95%9C%20HTTP%20%EC%9B%B9%20%EA%B8%B0%EB%B3%B8%20%EC%A7%80%EC%8B%9D/Section_5.MD#http-%EB%A9%94%EC%84%9C%EB%93%9C-%ED%99%9C%EC%9A%A9)
- [Section_6, HTTP 상태코드 2xx, 3xx 등](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EB%AA%A8%EB%93%A0%20%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%A5%BC%20%EC%9C%84%ED%95%9C%20HTTP%20%EC%9B%B9%20%EA%B8%B0%EB%B3%B8%20%EC%A7%80%EC%8B%9D/Section_6.MD#http-%EC%83%81%ED%83%9C%EC%BD%94%EB%93%9C)
- [Section_7, HTTP 헤더1 - 일반헤더](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EB%AA%A8%EB%93%A0%20%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%A5%BC%20%EC%9C%84%ED%95%9C%20HTTP%20%EC%9B%B9%20%EA%B8%B0%EB%B3%B8%20%EC%A7%80%EC%8B%9D/Section_7.MD#http-%ED%97%A4%EB%8D%941---%EC%9D%BC%EB%B0%98-%ED%97%A4%EB%8D%94)
- [Section_8, HTTP 헤더2 - 캐시와 조건부 요청](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EB%AA%A8%EB%93%A0%20%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%A5%BC%20%EC%9C%84%ED%95%9C%20HTTP%20%EC%9B%B9%20%EA%B8%B0%EB%B3%B8%20%EC%A7%80%EC%8B%9D/Section_8.MD#section_8)


# 스프링 MVC 1편 - 백엔드 웹 개발 핵심 기술
## section1
- [웹 서버, 웹 애플리케이션 서버](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20MVC1%ED%8E%B8%20-%20%EB%B0%B1%EC%97%94%EB%93%9C%20%EC%9B%B9%20%EA%B0%9C%EB%B0%9C%20%ED%95%B5%EC%8B%AC%20%EA%B8%B0%EC%88%A0/%EC%9B%B9%20%EC%84%9C%EB%B2%84%2C%20%EC%9B%B9%20%EC%95%A0%ED%94%8C%EB%A6%AC%EC%BC%80%EC%9D%B4%EC%85%98%20%EC%84%9C%EB%B2%84.MD#%EC%9B%B9-%EC%84%9C%EB%B2%84-%EC%9B%B9-%EC%95%A0%ED%94%8C%EB%A6%AC%EC%BC%80%EC%9D%B4%EC%85%98-%EC%84%9C%EB%B2%84)
- [서블릿](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20MVC1%ED%8E%B8%20-%20%EB%B0%B1%EC%97%94%EB%93%9C%20%EC%9B%B9%20%EA%B0%9C%EB%B0%9C%20%ED%95%B5%EC%8B%AC%20%EA%B8%B0%EC%88%A0/%EC%84%9C%EB%B8%94%EB%A6%BF.MD#%EC%84%9C%EB%B8%94%EB%A6%BF)
- [동시요청 멀티쓰레드](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20MVC1%ED%8E%B8%20-%20%EB%B0%B1%EC%97%94%EB%93%9C%20%EC%9B%B9%20%EA%B0%9C%EB%B0%9C%20%ED%95%B5%EC%8B%AC%20%EA%B8%B0%EC%88%A0/%EB%8F%99%EC%8B%9C%20%EC%9A%94%EC%B2%AD%20-%20%EB%A9%80%ED%8B%B0%EC%93%B0%EB%A0%88%EB%93%9C.MD#%EB%8F%99%EC%8B%9C-%EC%9A%94%EC%B2%AD---%EB%A9%80%ED%8B%B0%EC%93%B0%EB%A0%88%EB%93%9C)
- [HTML, HTTP API, CSR, SSR](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20MVC1%ED%8E%B8%20-%20%EB%B0%B1%EC%97%94%EB%93%9C%20%EC%9B%B9%20%EA%B0%9C%EB%B0%9C%20%ED%95%B5%EC%8B%AC%20%EA%B8%B0%EC%88%A0/HTML%2C%20HTP%20API%2C%20CSR%2C%20SSR.MD#html-htp-api-csr-ssr)
- [자바 백엔드 웹 기술 역사](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20MVC1%ED%8E%B8%20-%20%EB%B0%B1%EC%97%94%EB%93%9C%20%EC%9B%B9%20%EA%B0%9C%EB%B0%9C%20%ED%95%B5%EC%8B%AC%20%EA%B8%B0%EC%88%A0/%EC%9E%90%EB%B0%94%20%EB%B0%B1%EC%97%94%EB%93%9C%20%EC%9B%B9%20%EA%B8%B0%EC%88%A0%20%EC%97%AD%EC%82%AC.MD#%EC%9E%90%EB%B0%94-%EB%B0%B1%EC%97%94%EB%93%9C-%EC%9B%B9-%EA%B8%B0%EC%88%A0-%EC%97%AD%EC%82%AC)
- [스프링 MVC 전체구조](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20MVC1%ED%8E%B8%20-%20%EB%B0%B1%EC%97%94%EB%93%9C%20%EC%9B%B9%20%EA%B0%9C%EB%B0%9C%20%ED%95%B5%EC%8B%AC%20%EA%B8%B0%EC%88%A0/%EC%8A%A4%ED%94%84%EB%A7%81%20MVC%20%EC%A0%84%EC%B2%B4%EA%B5%AC%EC%A1%B0.MD#%EC%8A%A4%ED%94%84%EB%A7%81-mvc-%EC%A0%84%EC%B2%B4%EA%B5%AC%EC%A1%B0)
- [HTTP Message Conveter](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20MVC1%ED%8E%B8%20-%20%EB%B0%B1%EC%97%94%EB%93%9C%20%EC%9B%B9%20%EA%B0%9C%EB%B0%9C%20%ED%95%B5%EC%8B%AC%20%EA%B8%B0%EC%88%A0/HTTP%20%EB%A9%94%EC%8B%9C%EC%A7%80%20%EC%BB%A8%EB%B2%84%ED%84%B0.MD#http-%EB%A9%94%EC%8B%9C%EC%A7%80-%EC%BB%A8%EB%B2%84%ED%84%B0)

# 스프링 MVC 2편 - 백엔드 웹 개발 활용기술
- [Thymeleaf 소개](https://github.com/Hoonyyyy/Inflearn_Spring_YH/blob/main/%EC%8A%A4%ED%94%84%EB%A7%81%20MVC%202%ED%8E%B8%20-%20%EB%B0%B1%EC%97%94%EB%93%9C%20%EC%9B%B9%20%EA%B0%9C%EB%B0%9C%20%ED%99%9C%EC%9A%A9%20%EA%B8%B0%EC%88%A0/Thymeleaf%20%EC%86%8C%EA%B0%9C.MD#thymeleaf-%EC%86%8C%EA%B0%9C)







