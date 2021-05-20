---
layout: single
title: gudtjdvudrk
toc: true
toc_sticky: true
toc_label: "알아서 보십쇼"
---

### 72p
![p72](/assets/images/형성평가/p72.jpg)
~~~c
#include <stdio.h>
 
int main() {
 char name[11];
 int age;
 char code[2];
 float key;
 
 printf("이름을 입력하세요 : ");
 scanf("%s", name);
 printf("나이를 입력하세요 : ");
 scanf("%d", &age);
 printf("보안키를 입력하세요 : ");
 scanf("%f", &key);
 printf("부서코드를 입력하세요 : ");
 scanf("%c ", &code);
 
 printf("***********************\n");
 printf("이름 : %s\n", name);
 printf("나이 : %d\n", age);
 printf("부서코드 : %c \n", code);
 printf("보안키 : %.3f\n", key);
 printf("***********************\n");
 return 0;
}
~~~

### 76p
![20210407_141553](/assets/images/형성평가/20210407_141553.jpg)
~~~c
#include <stdio.h>
 
int main(void) {
 char fj[6];
 int a, b, c;
 float d, e, f;
 printf("***과목별 점수 계산 프로그램***\n");
 printf("어떤 과목입니까 :");
 scanf("%s", fj );
 printf("중간고사 반영비율/받은 점수를 입력하세요 : ");
 scanf("%f %d", &d, &a );
 printf("기말고사 반영비율/받은 점수를 입력하세요 : ");
 scanf("%f %d", &e, &b );
 printf("기말고사 반영비율/받은 점수를 입력하세요 : ");
 scanf("%f %d", &f, &c );
 printf("%s의 점수는 %.1f입니다\n", fj, a*d+b*e+c*f);
 return 0;
}
~~~

### 96p
![1](/assets/images/형성평가/1.jpg)
~~~c
#include <stdio.h>
 
int main(void) {
 int y, m, d, r;
 printf("생년 월 일을 차례대로 입력하세요 : ");
 scanf("%d %d %d", &y, &m, &d);
 r = (y-m+d)%10;
 if(r == 0)
   printf("당신의 사주는 대박입니다\n");
 else
   printf("당신의 사주는 그럭저럭입니다\n");
 return 0;
}
~~~

### 98p
![3](/assets/images/형성평가/3.jpg)
~~~c
#include <stdio.h>
 
int main(void) {
 int SUV_height;
 int th1, th2, th3;
 SUV_height=170;
 printf("터널 높이(cm)를 입력하세요 : th1 th2 th3\n");
 scanf("%d %d %d", &th1, &th2, &th3);
 if(SUV_height >= th1)
   printf("충돌 %d", th1);
 
 else if(SUV_height >= th2)
   printf("충돌 %d", th2);
  else if(SUV_height >= th3)
   printf("충돌 %d", th3);
  else
   printf("무사통과");
 return 0;
}
~~~
