---
layout: post
title:  " 서버 사이드 렌더링(SSR)과 클라이언트 사이드 렌더링(CSR) "
categories: Technology
author: goodGid
---
* content
{:toc}

## 렌더링이란?

* 어떠한 웹 페이지 접속시 그 페이지를 화면에 그려주는 것이다.










---

## SSR

![](/assets/img/posts/ssr_and_csr_1.png)

* SSR : Server Side Rendering

* 요청시마다 새로고침이 일어나며 서버에 새로운 페이지에 대한 요청을 하는 방식이다.

---

## CSR & SPA

![](/assets/img/posts/ssr_and_csr_2.png)

* CSR : Client Side Rendering

* SPA : Single Page Application

* 모바일 시대가 도래하면서 모바일 환경에 최적화된 서비스가 필요해졌다.

* 일반적인 컴퓨터에 비해 성능이 낮은 모바일에 최적화시키기 위해선 기존과는 다른 방법이 필요했다.

* 그래서 나온 개념이 **SPA(Single Page Application)**이다.

* SPA는 브라우저에 로드되고 난 뒤에 페이지 전체를 서버에 요청하는 것이 아니라 <br> **최초 한번 페이지 전체를 로딩**한 이후 부터는 데이터만 변경하여 사용할 수 있는 웹 애플리케이션을 의미한다. 

* 전통적인 웹 방식인 SSR은 SPA에 비해 성능이 뒤떨어졌다.

* 그 이유는 요청 시 마다 서버로부터 리소스를 받아 해석하고 화면에 렌더링하는 방식이기 때문이다.

* 이러한 점에 의해 SPA는 트래픽을 감소시키고 사용자에게 최적화된 환경을 제공할 수 있게 되었다.

* 서버는 단지 JSON 파일만 보내주는 역할을 하며 <br> html을 그리는 역할은 클라이언트 측에서 자바스크립트가 수행하였다. <br> 그리고 이것이 **클라이언트 사이드 렌더링(Client-side rendering)**이다.


---

> 주의할 점

* 전통적인 웹 페이지 방식 != SSR 

* SPA != CSR

* 전통적인 웹 페이지 방식이 SSR 방식을 사용한 것이고 <br> SPA가 CSR 방식을 사용한 것이다.


---

## SSR vs CSR

![](/assets/img/posts/ssr_and_csr_3.png)


### 초기 View 로딩 속도

* **SSR**의 경우 View를 서버에서 렌더링 하여 가져오기 때문에 **첫 로딩**이 매우 짧다. 

* 물론 JS파일을 모두 다운로드하고 적용하기 전까지는 <br> 그 어떤 인터랙션에도 반응하지 않지만 사용자 입장에서는 로딩이 매우 빠르다고 느낄 수 있다.

* 반면 **CSR**의 경우 서버에서 View를 렌더하지 않고 <br> HTML 다운 + JS파일 + 각종 리소스 다운을 받은 후 브라우져에서 렌더링을 하기 때문에 <br> SSR보다는 **초기 View 로딩 속도**는 오래걸린다.

* 그렇지만 CSR의 경우 사용자의 행동에 따라 필요한 부분만 다시 읽어들이기 때문에 <br> 서버 측에서 렌더링하여 전체 페이지를 다시 읽어들이는 것보다 빠른 인터랙션이 가능하다.

* 하지만 문제도 존재한다.

* CSR은 페이지를 읽어들이는 시간 + JS를 읽어들이는 시간 + 그리고 JS가 화면을 그리는 시간 <br> 위 작업이 완료 후 콘텐츠가 사용자에게 보여진다. 

* 여기에 웹 서버에서 콘텐츠 데이터라도 가져와야 한다면 그 시간은 더욱 길어진다.

* 즉 **초기 구동 속도**가 느리다는 **단점**이 존재하는 것이다.

* 물론 초기 구동 속도를 제외하면 그 다음부터는 **빠른 인터랙션**의 성능을 보인다.


---

### SEO 문제

* **SEO(검색 엔진 최적화)**의 문제가 존재한다.

* CSR방식으로 이루어진 사이트에서는 View를 생성하기위해 자바스크립트를 실행시켜야 한다.

* 하지만 대부분의 웹 크롤러 봇들은 자바스크립트 파일을 실행시키지 못한다.

* 때문에 HTML 에서만 콘텐츠를 수집하게 되고 CSR 페이지를 빈 페이지로 인식하게 된다. 


---

## 보안 문제

* **SSR**에서는 사용자에 대한 정보를 **서버 측**에서 **세션**으로 관리를 했다. 

* 그러나 **CSR**일 경우 **쿠키**말고는 사용자에 대한 정보를 저장할 공간이 마땅치 않다.


---


### 정리

* SSR의 경우 초기 로딩속도가 빠르고 SEO에 유리하지만 <br> View 변경시 서버에 계속 요청을 해야 하므로 서버에 부담이 크다.

* CSR의 경우 초기 로딩속도는 느리지만 <br> 초기 로딩 후에는 서버에 다시 요청할 필요없이 클라이언트 내에서 작업이 이루어지므로 매우 빠르다. <br> 하지만 SEO에 대한 문제가 있다.

* 추가로 SSR과 CSR MVC 구조를 가볍게 눈에 익혀두자.

![](/assets/img/posts/ssr_and_csr_4.png)




---

## Reference

* [서버 사이드 렌더링 그리고 클라이언트 사이드 렌더링](http://asfirstalways.tistory.com/244)

* [서버사이드 렌더링 , 클라이언트 사이드 렌더링](http://jaroinside.tistory.com/24)