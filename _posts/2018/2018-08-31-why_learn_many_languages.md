---
layout: post
title: 내가 다양한 언어를 익힌 이유
date: 2018-08-31 00:00:00
categories: [프로그래밍 언어]
tags: [프로그래밍 언어]
comments: true
---

최근에 이런 질문을 여러 차례 받았다.

>왜 그렇게 다양한 언어를 하세요?

나는 C언어로 프로그래밍을 시작했고 자연스레 C++을 하게 됐다.  

내가 프로그래밍을 배우던 시기나, 그리고 처음 취업을 했던 2005년 게임 업계에서 게임 개발을 위해선 차선이 없었다. C++을 제외한 언어는 툴 개발이나, 일부 스크립팅에 제한적으로 사용했을 뿐이다.

compile 환경을 통한 성능 차이, native 언어라는 성능상 장점을 배제하기 힘든 당시 상황적 제약 때문이었다.

네트웍 기반의 온라인 게임이 활성화 되면서 붉어진 서버 개발에서도 정확한 성능 측정과 임계치 파악, 베이스 라인 설정 등이 아주 중요하다. 

즉, 많은 어플리케이션 메트릭들을 최대한 계산된 영역으로 끌어내려야 하는데, managed언어도 잘 쓰려면 깊은 공부가 필요한데다가 양쪽 다 깊은 공부가 필요하다면 게임 업계에선 성능도 무척이나 중요하다고 보고 C++을 선택해온 것이라고 생각한다.

추가로 클라이언트와 유틸리티성 코드나 로직 코드를 공유할 수 있다는 점도 크게 작용했을 것이다.

그렇게 C++만 잘하면 될 것 같았던 나의 미래가, 모바일 시장이 열리면서 조금 달라졌다.

--- 

클라이언트 베이스의 게임이 다수 등장하고, 결과 저장을 위한 심플한 서버만 필요했던 시기가 되면서 웹서버가 도입됐다.

이전에는 GM툴 정도만 가동하던 웹서버로 게임 서비스를 진행하면서 다양한 언어가 게임 서버 개발 시장에 도입됐다.

자바, PHP, Node.js, Ruby on Rails 등… 다양한 언어로 구현된 웹서버로 게임이 서비스 되기 시작했다.

이 과정에서, 사내 스터디와 간단한 로그 분석 웹서버로 이용했던 Ruby on Rails를 나는 스타트 업에서 이용해서 서비스를 했고, 이후에는 Django를 통한 게임 서버를 구현하게 됐고, 성능상 이슈로 ASP.NET CORE로 포팅하게 됐었다.

이후 타의반 자의반으로 자바를 통한 게임 서버 개발을 하게 됐는데, 그 과정에서 자바를 익혔고 이후 웹 개발을 Spring Boot로 진행하면서 자바에 익숙해졌다.

사실 취미로 go랑 rust를 간단히 써보고 있었으나, 국내 개인 개발자 분들의 오픈소스가 워낙에 node.js, python, java에 편중되어 있다보니 포킹해서 작업 할 때는 해당 언어로 진행하면서, 더 익숙해진 감도 있다.

이렇게 익숙해진 일부 언어는 업무에서 사용할 기회로 이어지도록 노력하거나, 혹은 지속적으로 데브 토이로만 쓰게 되는 경우도 있다.

---

이렇게 다양한 언어에 대한 관심과 사용을 하는 이유는, 현대 언어는 서로 영향을 주고 받고 있는지, 어떠한 부분은 언어의 근본적 한계인지, 또 무엇에 대해 아쉬움을 느끼는지 알아야 내가 기술선정을 하게 될 때, 혹은 폴리글랏 프로그래밍을 해야 할 때 인지를 이해하고 싶어서였다.

이런 고민에 도움이 된 책은 임백준씨가 번역해주신 브루스 테이트의 세븐 랭귀지다.

그렇게 배우고나니 확실히 인사이트가 넓어졌다. 특히 C++만 파고들던 시기보다 훨씬 유연해졌다.

현대 개발은 바퀴를 재발명 하진 않지만, 자동차를 조립하기 위한 부품을 얼마나 잘 고르는지가 아주 중요한 문제다.

이는 유연함이 필요하다는 의미고, 그를 위해선 다양한 언어를 이해하고 있는 것이 필요하다.

**그를 위해서 시작했던 다양한 언어에 대한 이해, 기술에 대한 편견을 내려 놓는 데에 큰 도움이 됐다.**

그 것들이 앞으로의 내 발전에 큰 보탬이 될 요소라고 생각한다.

내가 종종 언급하는 얘긴데, 한국에서는 자바가 한국어 같은 느낌이다. 특정 업계 (게임, 보안, 네트워크 등)에서는 C++ 혹은 C언어지만, 그 비율이 다르다고나 할까?

하지만 내가 존경하는 대다수의 프로그래머는 자바만 (혹은 C++만) 잘하지 않는다.
잘 가져다 쓴다는 의미에는 상황에 따라 적합한 언어를 선정해야 한다는 의미도 큰 가치를 갖는다.

**결국 상황에 따라 폴리글랏 프로그래밍 해야 한다는 얘기다.**

자동화를 위해선, 혹은 서비스 로직을 위해선 가끔은 결합도가 낮게 작성한 스크립트 언어가 필요할 수 있다.

AWS 람다같은 서비스가 이에 대한 반증 중 하나라고 본다. 상황에 맞는 적절한 기술적 도입을 위해선, 기술에 대한 유연한 사고가 필요하다.

**기술의 발전이 어떠한 메커니즘과 기술적 가치를 중점에 두고 발전하고 있는지는 알아야 한다. 그래야 더 적은 코스트로 더 안정적인 서비스를 구축할 수 있고, 그게 더 현명하고 더 합리적인 판단이다.**

그래서 나는 다양한 언어를 익히려 시도했고, 큰 도움이 되고 있다. 내가 언급한 이런 부분에 대한 갈증과 아쉬움이 존재한다면 나와 같은 시도를 해보는게 어떨까?