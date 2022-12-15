---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_What_is_this
title: "Spring Webflux"

# post specific
# if not specified, .name will be used from _data/owner.yml
author: 공지혁
# multiple category is not supported
category: Spring
# multiple tag entries are possible
tags: [Spring]
# thumbnail image for post
img: "https://velog.velcdn.com/images/neity16/post/5679215a-8961-4529-9469-077f768c66d2/webflux.jpeg"
# disable comments on this page
#comments_disable: true

# publish date
date: 2022-11-25 10:04:30 +0900

# seo
# if not specified, date will be used.
#meta_modify_date: 2022-11-25 10:04:30 +0900
# check the meta_common_description in _data/lang/[language].yml
#meta_description: ""

# optional
# if you enabled image_viewer_posts you don't need to enable this. This is only if image_viewer_posts = false
#image_viewer_on: true
# if you enabled image_lazy_loader_posts you don't need to enable this. This is only if image_lazy_loader_posts = false
#image_lazy_loader_on: true
# exclude from on site search
#on_site_search_exclude: true
# exclude from search engines
#search_engine_exclude: true
# to disable this page, simply set published: false or delete this file
#published: false
---


![](https://velog.velcdn.com/images/neity16/post/5679215a-8961-4529-9469-077f768c66d2/webflux.jpeg)
# Webflux란
Spring Webflux란 spring5에서 새롭게 추가된 모듈이다.
Webflux는 클라이언트, 서버에서 reactive 스타일의 어플리케이션 개발을 도와주는 모듈이며, reactive-stack web framwork이며 non-blocking에 reactive stream을 지원합니다.

장점: 고성능, spring과 완벽한 통합, netty 지원, 비동기 non-blocking 메세지 처리
단점: 오류처리가 다소 복잡하다

## Spring MVC VS Spring Webflux
Spring MVC와 WebFlux의 공통점은 @Controller, Reactive 클라이언트입니다. 둘 다 Tomcat, Jetty, Undertow와 같은 서버에서 실행할 수 있습니다. Spring MVC에서는 명령형 논리, JDBC, JPA를 가질 수 있습니다. Spring WebFlux에서는 기능적 엔드 포인트, 이벤트 루프, 동시성 모델을 가질 수 있습니다. Spring WebFlux는 Netty 서버에서 실행할 수 있다는 장점이 있습니다.

![spring mvc vs spring webflux](https://docs.spring.io/spring-framework/docs/current/reference/html/images/spring-mvc-and-webflux-venn.png)


## Reference
[https://devuna.tistory.com/108](https://devuna.tistory.com/108)
[https://docs.spring.io/spring-framework/docs/current/reference/html/web-reactive.html#webflux](https://docs.spring.io/spring-framework/docs/current/reference/html/web-reactive.html#webflux)
