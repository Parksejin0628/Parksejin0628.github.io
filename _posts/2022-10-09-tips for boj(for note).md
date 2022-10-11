---
layout : single
title : "C++로 백준 문제를 풀 때 몇가지 팁들(메모용)"
---

C++로 백준 문제를 풀이할 때 몇가지 알아야 할 팁들, 숙지해야 할 사안 등을 메모하려고 한다.
문제풀이를 하며 알아낸 팁들을 앞으로도 꾸준히 써나가자.


# cin, cout 대신 printf, scanf 사용
수많은 문제 중에서 시간단축을 신경써야 하는 문제는 상당히 많다.\
그런데, C++에서 지원하는 cin, cout은 **연산속도가 매우 느리다**는 단점이 존재한다.\
따라서, 문제 풀이에서 요구하는 시간 복잡도를 맞추더라도 시간초과하는 경우가 빈번하게 발생한다.\
include<cstdio>를 선언하고 **비교적 연산속도가 빠른 printf, scanf**를 사용하도록 하자.

# pragma warning(disable:4996)
scanf와 cstring 라이브러리에 있는 각종 함수들을 Visual Stduio에서 사용하게 되면 에러가 발생하며 컴파일을 허용하지 않는다.\
이는 scanf가 안전하지 않아 Visual Stduio에서 자체적으로 금지했기 때문이다.\
백준 문제를 풀이할 때는 이 문제에 대해 신경쓸 필요가 없으므로 불필요한 에러가 된다.\
따라서, 코드의 맨 앞줄에 **#pragma warning(disable:4996)선언 혹은 #define _CRT_SECURE_NO_WARNINGS**을 선언해야 한다.
