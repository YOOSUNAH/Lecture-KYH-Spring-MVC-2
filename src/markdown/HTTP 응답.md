### HTTP 응답 - 정적 리소스, 뷰 템플릿
응답 데이터는 이미 앞에서 일부 다룬 내용들이지만, 응답 부분에 초점을 맞추어서 정리해보자.
스프링(서버)에서 응답 데이터를 만드는 방법은 크게 3가지이다.

* 정적 리소스
  * 예) 웹 브라우저에 정적인 HTML, css, js를 제공할 때는, 정적 리소스를 사용한다.
* 뷰 템플릿 사용
  * 예) 웹 브라우저에 동적인 HTML을 제공할 때는 뷰 템플릿을 사용한다.
* HTTP 메시지 사용
  * HTTP API를 제공하는 경우에는 HTML이 아니라 데이터를 전달해야 하므로, HTTP 메시지 바디에 JSON 같은 형식으로 데이터를 실어 보낸다.

#### 정적 리소스
* 스프링 부트는 클래스패스의 다음 디렉토리에 있는 정적 리소스를 제공한다. 
* `/static` , `/public` , `/resources` , `/META-INF/resources`
* `src/main/resources` 는 리소스를 보관하는 곳이고, 또 클래스패스의 시작 경로이다. 
* 따라서 다음 디렉토리에 리소스를 넣어두면 스프링 부트가 정적 리소스로 서비스를 제공한다.

#### 정적 리소스 경로
`src/main/resources/static`
다음 경로에 파일이 들어있으면
`src/main/resources/static/basic/hello-form.html`
웹 브라우저에서 다음과 같이 실행하면 된다. 
`http://localhost:8080/basic/hello-form.html`
정적 리소스는 해당 파일을 변경 없이 그대로 서비스하는 것이다.

#### 뷰 템플릿
뷰 템플릿을 거쳐서 HTML이 생성되고, 뷰가 응답을 만들어서 전달한다.
일반적으로 HTML을 동적으로 생성하는 용도로 사용하지만, 다른 것들도 가능하다. 뷰 템플릿이 만들 수 있는 것이라면 뭐든지 가능하다.

스프링 부트는 기본 뷰 템플릿 경로를 제공한다.
#### 뷰 템플릿 경로
`src/main/resources/templates`
#### 뷰 템플릿 생성
`src/main/resources/templates/response/hello.html`
  