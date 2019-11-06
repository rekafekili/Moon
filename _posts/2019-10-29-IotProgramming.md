---
layout: post
title: "IoT프로그래밍 - DTD"
date: 2019-10-29
excerpt: "DTD 의 개념을 알고 적용해 볼 수 있다."
tags: [IoT프로그래밍, DTD]
comments: true
---

# Chapter 6 - Document Type Definition(DTD)

## 6.1 Introduction
- XML Document 의 타입을 정의(어떤 요소, 어떤 속성 등등)
- EBNF(Extended Backus-Naur Form) 문법을 사용
- DTD 가 반드시 필요한 것은 아니지만 권장하는 편이다.

## 6-2. Parsers, Well-formed and Valid XML Documents
- __Parsers__
  - Validating
    - DTD를 읽을 수 있는지 확인
    - XML Document 가 DTD 에 따라 잘 구성된 경우
      - Document 가 Well-formed 이어도 Valid 가 아닐 수도 있다.
  - NonValidating
    - DTD를 읽을 수 있는지 확인
    - 형식적으로 DTD에 따라 Document 를 확인 할 수 없는 경우

## 6-3. Document Type Declaration

## 6-4. Element Type Declaration
``` xml
<!-- Fig. 6.2 : intro.dtd -->
<!-- External Declarations -->

<!ELEMENT myMessage ( message )>
<!ELEMENT myMessage ( #PCDATA )>
```
_#PCDATA : Parcable Character DATA, 즉 파싱 가능한 문자열을 뜻한다._

``` xml
<?xml version = "1.0">

<!-- Fig. 6.1 : intro.xml -->
<!-- Using an external subnet -->

<!DOCTYPE myMessage SYSTEM "intro.dtd">

<myMessage>
  <>
</myMessage>

```