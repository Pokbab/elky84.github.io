---
layout: post
title: 멀티스레드 프로그래밍시 유의점
date: 2010-02-23 11:14:54
categories: 병렬프로그래밍
comments: true
---

1. 데이터를 동시에 쓰는 상황, 읽는 도중 값이 변경되는 상황, 읽는 도중 delete 되는 상황에 유의하라.
* 데이터를 동적으로 다뤄야 되는 상황 자체를 줄이는 것이 좋다. NULL 대신 NULL객체 처리를 선호하는 것이 멀티 스레드 프로그래밍에서 크래시를 줄이고 쉽게 예외 핸들링 할 수 있는 방법중 하나다.
2. 생성자 / 소멸자 호출 도중에 가상 함수를 읽지 않게 하라.
* 가급적 생성자 / 소멸자에선 로직 처리를 금하라. 실패 할 수 있는 동작은 생성자/소멸자에서 시도하지 않는 것이 좋다.

3. 동기화에 대해 주의하라. 
* 어디서부터 어디까지 공유 데이터인지를 명확히하고, 그 이상의 접근을 막아라.

4. 스레드 마다 별도로 주어지는 공간 (스택), 모든 스레드가 공유하는 공간 (힙, 정적 데이터 영역) 등에 대해 파악하고 코드를 작성하라.
* 스레드 프로그래밍에서 static 객체는 특히나 자주 말썽을 썩인다. static한 코드를 의심하라.

5. 어설픈 가정은 하지 말라. 데이터가 겹치지 않을 것이라는 가정을 하고 있다면, 실제로 겹치지 않도록, 겹치게 된다면 미리 알 수 있도록 하라.
* 특히 코딩을 하는 과정에서, 잘못된 스레드 용법이 쉽게 작성 가능한 구조라면, 그 작업 자체가 불가능하거나 감지 되도록 강제하라.

6. 락 정책에 주의하라. 
* 리터럴 변수에만 사용할 것이라면 Interlockedxxx 계열 함수만 사용하면 된다. 
* 만약 리터럴이 아니라 구조체나 클래스에서 사용하고, 락이 걸린 영역 내에서 메소드를 호출하게 될 경우 데드락 등의 문제로 악몽을 겪을 수 있으니 주의하자.