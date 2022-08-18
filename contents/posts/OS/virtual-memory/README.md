---
title: "가상 메모리(Virtual Memory)"
description:
date: 2022-08-16
tags:
- os
- linux
- virtual-memory
- memory
- series: "운영체제"
---

> "가상 메모리는 크기가 다른 물리 메로리에서 일관되게 프로세스를 실행할 수 있는 기술이다"

> 가상 메모리 시스템에서 스왑 영역은 하드디스크에 존재하지만 메모리 관리자가 관리하는 영역으로서 메모리의 이룹이며, 가상 메모리의 구성 요소 중 하나이다.
메모리 관리자는 물리 메로리의 부족한 부분을 스오바 영역으로 보충한다.
즉 물리 메모리가 꽉 찻을 때 일부 프로세스를 스왑 영역으로 보내고(스왑아웃), 몇 개의 프로세스가 작업을 마치면 스왑 영역에 있는 프로세스를 메모리로 가져온다(스왑인).