---
title: "혼자 공부하는 컴퓨터구조+운영체제(1-2) - 컴퓨터 구조의 큰 그림"
date: 2022-10-26 04:00:00
tags:
- 학습기록
- 컴퓨터구조
- CPU
- RAM
- 데이터
- 명령어
series: "혼자 공부하는 컴퓨터 구조+운영체제"
---

# 01-2. 컴퓨터 구조의 큰 그림

> 컴퓨터 구조 지식은 크게 두 가지입니다. 하나는 '**컴퓨터가 이해하는 정보**'이고 또 하나는 ‘**컴퓨터의 네 가지 핵심 부품**’입니다.

## 컴퓨터가 이해하는 정보

컴퓨터는 0과 1로 표현된 정보만을 이해합니다. 0과 1로 표현되는 정보에는 크게 두 종류가 있는데, 바로 `데이터`와 `명령어`입니다.

### **데이터(Data)**

데이터는 컴퓨터가 이해하는 숫자, 문자, 이미지, 동영상과 같은 정적인 정보입니다.
컴퓨터와 주고받는 정보나 컴퓨터에 저장된 정보를 데이터라 통칭하기도 합니다.

### **명령어(Instruction)**

명령어는 데이터를 움직이고 컴퓨터를 작동시키는 정보입니다. 데이터와 명령어 중 더 중요한 정보는 명령어입니다. 데이터는 명령어 없이는 아무것도 할 수 없는 정보 덩어리일 뿐이기 때문입니다.

즉, 명령어는 컴퓨터를 작동시키는 정보이고, 데이터는 명령어를 위해 존재하는 일종의 재료라고 할 수 있습니다.

> "**컴퓨터는 도대체 뭘까**?"라는 질문에 한 마디로 답해보자면 `컴퓨터는 명령어를 처리하는 기계`라고 할 수 있습니다.

## 컴퓨터의 4가지 핵심 부품

컴퓨터를 이루고 있는 네 가지 핵심 부품은 `중앙처리장치(CPU: Central Processing Unit)`, `주기억장치(Main Memory)`, `보조기억장치(Secondary Storage)`, `입출력장치(Input/Output Device)`입니다.

## 중앙처리장치(CPU)

CPU는 컴퓨터의 두뇌입니다. CPU는 메모리에 저장된 명령어를 읽어 들이고, 읽어 들인 명령어를 해석하고, 실행하는 부품입니다. 즉, 컴퓨터에서 명령어를 읽고 연산을 수행하는 것은 CPU입니다.

CPU의 역할과 작동 원리를 구체적으로 이해하기 위해서는 CPU 내부 구성 요소 중 가장 `중요한 산술논리연산장치(ALU: Arithmetic Logic Unit)`, `레지스터(Register)`, `제어장치(CU: Centrol Unit)`에 대해 알아야 합니다.

### 산술논리연산장치(ALU)

ALU는 쉽게 말해 계산기로 계산만을 위해 존재하는 부품입니다. 컴퓨터 내부에서 수행되는 대부분의 계산을 수행합니다.

### 레지스터(Register)

레지스터는 CPU 내부의 작은 임시 저장 장치입니다. 프로그램을 실행하는 데 필요한 값들을 임시로 저장하며, CPU 내부에는 여러 개의 레지스터가 존재하고 각기 다른 이름과 역할을 가지고 있습니다.

### 제어장치(CU)

제어장치는 제어 신호(Control Signal)라는 전기 신호를 내보내고 명령어를 해석하는 장치입니다. 시스템 버스 중 제어 버스를 이용하여 메모리를 향해 '메모리 읽기', '메모리 쓰기'와 같은 제어신호를 보내는 장치입니다.

> "**누가 명령어를 읽고 연산을 수행하는가?**"라는 질문에는 `CPU`라고 대답할 수 있습니다.

## 메모리

메모리는 현재 실행되는 프로그램의 명령어와 데이터를 저장하는 부품입니다. 즉, 프로그램이 실행되려면 반드시 메모리에 저장되어 있어야 합니다.

메모리는 현실에서 우리가 주소로 원하는 위치를 찾아갈 수 있듯이 컴퓨터에서도 메모리에 저장된 값에 빠르고 효율적으로 접근하기 위해 주소라는 개념을 사용하여 메모리 내 원하는 위치에 접근할 수 있습니다.

> 메모리는 보통 RAM(Random Access Memory)를 지칭합니다.

> "**어디에서 명령어를 읽는가?**"라는 질문에는 `RAM`이라고 대답할 수 있습니다.

## 보조기억장치

앞서 메모리는 실행되는 프로그램의 명령어와 데이터를 저장한다고 했지만, 두 가지 치명적인 약점이 있습니다. 첫재는 가격이 비싸 저장 용량이 적다는 점이고, 둘째는 전원이 꺼지면 저장된 내용을 읽는다는 점입니다.

메모리보다 값이 저렴하며 저장용량이 크고 전원이 꺼져도 저장된 내용을 읽지 않으며, 메모리를 보조하는 저장 장치가 보조조기억장치입니다.

하드 디스크, SSD, USB 메모리 DVD, CD-ROM과 같은 저장 장치가 보조기억장치의 일종입니다.

> 메모리가 현재 '실행되는' 프로그램을 저장한다면, 보조기억장치는 '보관할' 프로그램을 저장한다고 생각해도 좋습니다.


## 입출력장치

입출력장치는 마이크, 스피커, 프린터, 마우스, 키보드 처럼 컴퓨터 외부에 연결되어 컴퓨터 내부와 정보를 교환하는 장치를 의미합니다.

## 참고

- [http://www.yes24.com/Product/Goods/111378840](http://www.yes24.com/Product/Goods/111378840)
- [https://youtu.be/_uByLEwOt7Q](https://youtu.be/_uByLEwOt7Q)