# 웹기초 

## 요청과 응답 이해하기

![image](https://github.com/somi9954/web_basic/assets/137499604/d9173031-2e03-40a9-aefb-9afe4e2bd2f8)


- **요청(request)** :브라우저에서 서버에 자원을 요청하는 것이다
- **응답(response)** : 서버(server) 에서 요청한 자원을 응답하는 것이다.
- 서버는 클라이언트가 있기에 동작합니다. 클라이언트에서 서버로 요청(request)을 보내고, 서버에서는 요청의 내용을 읽고 처리한 뒤 클라이언트에 응답(response)을 보냅니다.
- 따라서 서버에는 요청을 받는 부분과 응답을 보내는 부분이 있어야 합니다. 요청과 응답은 이벤트 방식이라고 생각할 수 있습니다.

## HTTP(HyperText Transfer Protocol)

- html문서를 전송하고 수신하는 프로토콜이다.
- HTTP는 HTML 문서와 같은 리소스들을 가져올 수 있도록 해주는 프로토콜입니다. HTTP는 웹에서 이루어지는 모든 데이터 교환의 기초이며, 클라이언트-서버 프로토콜이기도 합니다. 클라이언트-서버 프로토콜이란 (보통 웹브라우저인) 수신자 측에 의해 요청이 초기화되는 프로토콜을 의미합니다. 하나의 완전한 문서는 텍스트, 레이아웃 설명, 이미지, 비디오, 스크립트 등 불러온(fetched) 하위 문서들로 재구성됩니다.
- 클라이언트와 서버들은 (데이터 스트림과 대조적으로) 개별적인 메시지 교환에 의해 통신합니다. 보통 브라우저인 클라이언트에 의해 전송되는 메시지를 요청(requests)이라고 부르며, 그에 대해 서버에서 응답으로 전송되는 메시지를 응답(responses)이라고 부릅니다.

![https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/4.Servlet%20%26%20JSP1(21%EC%8B%9C%EA%B0%84)/1%EC%9D%BC%EC%B0%A8(3h)%20-%20%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD%20%EA%B5%AC%EC%B6%95%2C%20%EC%9B%B9%20%EA%B8%B0%EC%B4%88%2C%20%EC%84%9C%EB%B8%94%EB%A6%BF(Servlet)/images/images16.png](https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/4.Servlet%20%26%20JSP1(21%EC%8B%9C%EA%B0%84)/1%EC%9D%BC%EC%B0%A8(3h)%20-%20%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD%20%EA%B5%AC%EC%B6%95%2C%20%EC%9B%B9%20%EA%B8%B0%EC%B4%88%2C%20%EC%84%9C%EB%B8%94%EB%A6%BF(Servlet)/images/images16.png)

```java
💡참고
ftp(file Transfer Protocol) : 파일을 전송하고 수신할 수 있는 프로토콜
```


## 헤더(header)

HTTP 헤더는 클라이언트와 서버가 요청 또는 응답으로 부가적인 정보를 전송할 수 있도록 해줍니다. HTTP 헤더는 대소문자를 구분하지 않는 이름과 콜론 ':' 다음에 오는 값(줄 바꿈 없이)으로 이루어져있습니다. 값 앞에 붙은 빈 문자열은 무시됩니다.

- **일반 헤더(General header)** : 요청과 응답 모두에 적용되지만 바디에서 최종적으로 전송되는 데이터와는 관련이 없는 헤더.
- **요청헤더(Request header)**: 페치될 리소스나 클라이언트 자체에 대한 자세한 정보를 포함하는 헤더. → 서버쪽에서 자원을 조회하기 위한 정보를 확인하기 위해 참고해야 할 사항 : 요청 쪽에 대한 정보
    - 요청 방식(method-GET,POST)
    - 요청 주소
    - 쿠키
    
  ![image](https://github.com/somi9954/web_basic/assets/137499604/2c8c21d8-599c-4db5-a2a7-905f4deb0ef2)

  ![image](https://github.com/somi9954/web_basic/assets/137499604/32020c5e-b817-4d57-a10d-00815dd8bea5)

    
    - 요청 IP
    - 브라우저 언어 설정
    
   ![image](https://github.com/somi9954/web_basic/assets/137499604/81b0b10b-cb89-434a-9b69-fe49f8b395ab)

    ![image](https://github.com/somi9954/web_basic/assets/137499604/51e32815-8e55-4651-b70f-8722621315a4)

    
    - 브라우저 종류(User-Agent) : 웹과 모바일시 차이가 있다.
    
    ![image](https://github.com/somi9954/web_basic/assets/137499604/16ad13ea-2674-4e99-982b-aea29a32b633)

    
    ![image](https://github.com/somi9954/web_basic/assets/137499604/94e8da91-70b6-495c-adee-f599a9911329)

    
    - 요청 데이터의 형식
    content-type:
      content-type : application/x-www-form-urlencoded;
    application/json;
    - Referer : 직전 경로를 확인할 수 있다 →  광고에 대한 통계로 사용이 가능하다.
    
    ![image](https://github.com/somi9954/web_basic/assets/137499604/380f1fdf-91ff-4d22-a2a8-d27b278ed4fb)

    
- **응답헤더(Response header)**
    - 위치 또는 서버 자체에 대한 정보(이름, 버전 등)와 같이 응답에 대한 부가적인 정보를 갖는 헤더.
    - 응답 바디의 데이터 종류
    - content-type : text/html → 브라우저가 바디 데이터를 해석하기 위한 정보
    - 응답 상태 코드 </br>
    2xx </br>
    200(OK): 정상 응답 (브라우저 요청 →서버 → 응답)</br>
    201(CREATE): 작성됨(POST 방식 ) : 데이터를 서버에 기록을 완료</br>
        
        
      3xx</br>
        301: 영구 이동</br>
        302: 임시 이동</br>
        
       예) 일반 pc 사이트에서 모바일로 사용시 나타난다.
        
        ![image](https://github.com/somi9954/web_basic/assets/137499604/04d9a057-863b-44bc-a665-b650e9f3bfd6)

        
        일반 피씨 사용시에는 응답 상태 코드가 200으로 정상 코드가 나오게 된다.</br>
        
        하지만 pc버전에서 모바일로 변환하게 되면  302 코드로 상태가 변화가 된다. 
        
       ![image](https://github.com/somi9954/web_basic/assets/137499604/73ec124b-8f8c-4fb1-9e8d-f1a799dda03f)

        ![image](https://github.com/somi9954/web_basic/assets/137499604/739b9128-4d1d-4cd3-89b2-89381adbd03f)

       왜냐하면 www.naver.com에서의 응답헤더에서 서버쪽으로 브라우저에 명령하게 되어 페이지 이동을 하게 한다. 이동하게 하면 임시 이동 코드 302로 나오게 된다.</br>
        304: 캐시됨. 동일한 주소로 되어 있는 파일 -> 임시로 저장, 서버에 요청 → 일정시간 경과 후 삭제 다시 요청 → 서버에 부담이 덜 가게 된다.
        
        4xx : 클라이언트 오류</br>
        400 : 잘못된 요청(Bad Request) => 요청 데이터를 정해진 대로 전송하지 않은 경우</br>
        401 : 접속 권한 없음(Unauthorized)</br>
        403 : 금지됨(forbidden)</br>
        404 : 페이지 없음 (NOT Found)</br>
        405 : Method Not Allowed - GET, POST, DELETE, PUT, DELETE
        
        5xx : 서버쪽 오류
        
        500 : 소스 코드의 오류(Internal Server Error)</br>
        501 : Bad Gateway</br>
        503 : 서비스를 이용할 수 없음(Service Unavailable)
        
    - 응답 서버쪽 정보
        - 서버쪽에서 브라우저 전달하는 명령
        - cache-control
        - Location : 주소 -> 서버에서 →브라우저가 주소 이
        - refresh : 초 - 초 마다 새로고침
        - Set-Cookie: 키= 값; 키= 값;:: 브라우저에게 쿠키값을 저장해달라 요청
        - Content-disposition: attachment; filename = ..  → 바디 출력 흐름 파일로 변경 ⇒ 파일 다운로드
- **엔티티 헤더(Entity header)**: 컨텐츠 길이나 MIME 타입과 같이 엔티티 바디에 대한 자세한 정보를 포함하는 헤더.

## 바디(body)

HTTP Request가 전송하는 데이터를 담고 있는 부분. 전송하는 데이터가 없다면 body 부분은 비어있습니다.

보통 post 요청일 경우, HTML 폼 데이터가 포함되어 있습니다.

- **요청바디(Request body)**:POST 방식으로 데이터를 전송
    
    ```html
    application/x-www-form-urlencoded;
    		subject=%EC%A0%9C%EB%AA%A9&content=%EC%95%99
    		-> 16진수 방식을 urlencoded 방식으로 UTF-8로 변환 
         
    		application/json;
    		{ "subject": "제목","content": "내용" }
       -> content-type:
        content-type : application/x-www-form-urlencoded;
         application/json 로 변환
    ```
    
- **응답바디(Response body)**
    - 서버 데이터를 응답 받는다
    

### HTTP 요청/응답

![https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/4.Servlet%20%26%20JSP1(21%EC%8B%9C%EA%B0%84)/1%EC%9D%BC%EC%B0%A8(3h)%20-%20%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD%20%EA%B5%AC%EC%B6%95%2C%20%EC%9B%B9%20%EA%B8%B0%EC%B4%88%2C%20%EC%84%9C%EB%B8%94%EB%A6%BF(Servlet)/images/images17.png](https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/4.Servlet%20%26%20JSP1(21%EC%8B%9C%EA%B0%84)/1%EC%9D%BC%EC%B0%A8(3h)%20-%20%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD%20%EA%B5%AC%EC%B6%95%2C%20%EC%9B%B9%20%EA%B8%B0%EC%B4%88%2C%20%EC%84%9C%EB%B8%94%EB%A6%BF(Servlet)/images/images17.png)

- 요청과 응답은 모두 **헤더와 본문**을 가지고 있습니다. **헤더는 요청 또는 응답에 대한 정보를 가지고 있는 곳**이고 **본문은 서버와 클라이언트 간에 주고받을 실제 데이터를 담아두는 공간**입니다.
- 개발자 도구의 Network 탭에서 요청 중 하나를 클릭해보면 더 상세하게 요청과 응답을 살펴볼 수 있습니다.

### 요청의 헤더와 본문

![https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/4.Servlet%20%26%20JSP1(21%EC%8B%9C%EA%B0%84)/1%EC%9D%BC%EC%B0%A8(3h)%20-%20%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD%20%EA%B5%AC%EC%B6%95%2C%20%EC%9B%B9%20%EA%B8%B0%EC%B4%88%2C%20%EC%84%9C%EB%B8%94%EB%A6%BF(Servlet)/images/images18.png](https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/4.Servlet%20%26%20JSP1(21%EC%8B%9C%EA%B0%84)/1%EC%9D%BC%EC%B0%A8(3h)%20-%20%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD%20%EA%B5%AC%EC%B6%95%2C%20%EC%9B%B9%20%EA%B8%B0%EC%B4%88%2C%20%EC%84%9C%EB%B8%94%EB%A6%BF(Servlet)/images/images18.png)

- General은 공통 헤더이고, Request Headers는 요청의 헤더, Response Headers는 응답의 헤더입니다.
- Request Payload가 요청의 본문입니다. 응답의 본문은 Preview나 Response 탭에서 확인할 수 있습니다.

### 응답의 본문

![https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/4.Servlet%20%26%20JSP1(21%EC%8B%9C%EA%B0%84)/1%EC%9D%BC%EC%B0%A8(3h)%20-%20%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD%20%EA%B5%AC%EC%B6%95%2C%20%EC%9B%B9%20%EA%B8%B0%EC%B4%88%2C%20%EC%84%9C%EB%B8%94%EB%A6%BF(Servlet)/images/images19.png](https://raw.githubusercontent.com/yonggyo1125/curriculum300H/main/4.Servlet%20%26%20JSP1(21%EC%8B%9C%EA%B0%84)/1%EC%9D%BC%EC%B0%A8(3h)%20-%20%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD%20%EA%B5%AC%EC%B6%95%2C%20%EC%9B%B9%20%EA%B8%B0%EC%B4%88%2C%20%EC%84%9C%EB%B8%94%EB%A6%BF(Servlet)/images/images19.png)

### HTTP 상태 코드

브라우저는 서버에서 보내주는 상태 코드를 보고 요청이 성공했는지 실패했는지를 판단합니다.

- **2XX** : 성공을 알리는 상태코드 입니다. 대표적으로 200(성공), 201(작성됨)이 많이 사용됩니다.
- **3XX** : 리다이렉션(다른 페이지로 이동)을 알리는 상태 코드 입니다. 어떤 주소를 입력했는데 다른 주소의 페이지로 넘어갈 때 이 코드가 사용됩니다. 대표적으로 301(영구이동), 302(임시 이동)가 있습니다. 304(수정되지 않음)는 요청의 응답으로 캐시를 사용했다는 뜻 입니다.
- **4XX** : 요청 오류를 나타냅니다. 요청 자체에 오류가 있을 때 표시됩니다. 대표적으로 400(잘못된 요청), 401(권한없음), 403(금지됨), 404(찾을 수 없음)가 있습니다.
- **5XX** : 서버오류를 나타냅니다. 요청은 제대로 왔지만 서버에 오류가 생겼을 때 발생합니다. 이 오류가 뜨지 않게 주의해서 프로그래밍 해야 합니다. 500(내부 서버 오류), 501(불량 게이트웨이), 503(서비스를 사용할 수 없음)이 자주 사용됩니다.

## HTTP 요청 메서드

클라이언트가 서버에 데이터를 전송하여 응답을 요청할때 사용하는 방식

- GET : 서버 자원을 가져오고자 할 때 사용합니다. 요청의 본문에 데이터를 넣지 않습니다. 데이터를 서버로 보내야 한다면 쿼리스트링을 사용합니다.
    - 요청 URL 주소를 경로를 검색하여 서버의 자원을 조회 할 수 있다.
    
   ![image](https://github.com/somi9954/web_basic/assets/137499604/ea75f698-9748-4362-9668-13b82847da05)

    
    - 요청 URL 주소를 웹사이트 주소창에 검색을 하게 되면 원하는 데이터를 조회할 수 있다.
    
    ![image](https://github.com/somi9954/web_basic/assets/137499604/a873cf3d-7259-47d9-91a1-06646d69fa01)

    
    ```java
    https://news.naver.com/main/main.naver?mode=LSD&mid=shm&sid1=105 
    네이버 뉴스 it/과학 영역 조회
    
    https://news.naver.com/
    	    main/main.naver
    		?
    		mode=LSD        쿼
    		&               리
    		mid=shm         스
    		&                트
    		sid1=105         링
    ```
    
    - 쿼리 스트링 (querystring)
        - 서버쪽에서 질의(query)하기 위한 데이터
        - 웹개발에서 데이터를 요청하는 방식 중 주로 GET방식으로 데이터를 요청할 때 쓰이는 방법.
        - URL주소뒤에 물음표(?)를 붙이고 key1=value1&key2=value2...방식으로 데이터를 요청한다.
        - 주소에 조회용 데이터가 있다. ⇒ 요청 body는 비어 있는 상태로 전송.
- POST : 서버에 자원을 새로 등록하고자 할 때 사용합니다. 요청의 본문에 새로 등록할 데이터를 넣어 보냅니다.
    - 요청 헤더 content-type
        - 요청 데이터 body에 기록
    
    ```java
    예)
    content-type: application/x-www-form-urlencoded;
    	subject=%EC%A0%9C%EB%AA%A9&content=%EC%95%99 = 16 진수
    	URL 인코딩

    참고) 
    	content-type: application/json
        ("키": "값","키": "값")
    {"subject" : "...", "content" : "..."}
    ```
    
- PUT(POST 일종) : 서버의 자원을 요청에 들어 있는 자원으로 치환하고자 할 때 사용합니다. 요청의 본문에 치환할 데이터를 넣어 보냅니다.
- PATCH(POST 일종) : 서버 자원의 일부만 수정하고자 할 때 사용합니다. 요청의 본문에 일부 수정할 데이터를 넣어 보냅니다.
- DELETE (GET방식): 서버의 자원을 삭제하고자 할 때 사용합니다. 요청의 본문에 데이터를 넣지 않습니다.
- OPTIONS : 요청(GET,POST)을 하기 전에 통신 옵션을 설명하기 위해 사용합니다.

> GET 메서드 같은 경우네는 브라우저에서 캐싱(기억)할 수도 있으므로 같은 주소로 GET 요청을 할 때 서버에서 가져오는 것이 아니라 캐시에서 가져올 수도 있습니다.
> 

-----
참고: https://engineerinsight.tistory.com/470

참고: https://goddaehee.tistory.com/169

참고: https://code-overflow.tistory.com/category/HTTP?page=1

참고: https://velog.io/@bky373/Web-HTTP%EC%99%80-HTTPS-%EC%B4%88%EA%B0%84%EB%8B%A8-%EC%A0%95%EB%A6%AC

참고: https://doqtqu.tistory.com/286

참고: https://bomz.tistory.com/13

참고: https://velog.io/@rlawogks2468/%EC%BF%BC%EB%A6%AC%EC%8A%A4%ED%8A%B8%EB%A7%81Query-String%EC%9D%B4%EB%9E%80

참고: https://github.com/yonggyo1125
