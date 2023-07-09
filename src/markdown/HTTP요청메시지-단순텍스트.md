
#### 스프링 MVC는 다음 파라미터를 지원한다.
* InputStream(Reader): HTTP 요청 메시지 바디의 내용을 직접 조회
* OutputStream(Writer): HTTP 응답 메시지의 바디에 직접 결과 출력

#### 스프링 MVC는 다음 파라미터를 지원한다.
* HttpEntity: HTTP header, body 정보를 편리하게 조회
* 메시지 바디 정보를 직접 조회
* 요청 파라미터를 조회하는 기능과 관계 없음 @RequestParam X, @ModelAttribute X
* HttpEntity는 응답에도 사용 가능
* 메시지 바디 정보 직접 반환
* 헤더 정보 포함 가능
* view 조회X

#### @RequestBody
* @RequestBody 를 사용하면 HTTP 메시지 바디 정보를 편리하게 조회할 수 있다.
* 참고로 헤더 정보가 필요하다면 HttpEntity 를 사용하거나 @RequestHeader 를 사용하면 된다.

* 이렇게 메시지 바디를 직접 조회하는 기능은 요청 파라미터를 조회하는 @RequestParam , @ModelAttribute 와는 전혀 관계가 없다.

#### 요청 파라미터 vs HTTP 메시지 바디
* 요청 파라미터를 조회하는 기능: @RequestParam , @ModelAttribute HTTP 
* 메시지 바디를 직접 조회하는 기능: @RequestBody

#### @ResponseBody
* @ResponseBody 를 사용하면 응답 결과를 HTTP 메시지 바디에 직접 담아서 전달할 수 있다. 
* 물론 이 경우에도 view를 사용하지 않는다.

