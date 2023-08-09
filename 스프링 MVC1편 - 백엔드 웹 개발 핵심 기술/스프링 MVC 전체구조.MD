# 스프링 MVC 전체구조

## DispatcherServlet
- DispacherServlet 도 부모 클래스에서 HttpServlet 을 상속 받아서 사용하고, 서블릿으로 동작한다.
  - DispatcherServlet FrameworkServlet HttpServletBean HttpServlet
- 스프링 부트는 DispacherServlet 을 서블릿으로 자동으로 등록하면서 모든 경로( urlPatterns="/" )에 대해서 매핑한다.
  - 참고: 더 자세한 경로가 우선순위가 높다. 그래서 기존에 등록한 서블릿도 함께 동작한다.


- 나머지 스프링MVC 구조의 이해 pdf에서 보기















