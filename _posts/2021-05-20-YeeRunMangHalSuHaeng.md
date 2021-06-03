---
layout: single
title: 수행평가 
toc: true
toc_sticky: true
toc_label: "알아서 보십쇼"
---

### 72p 보안코드 입력
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

### 76p 과목별 점수 계산 프로그램
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

### 96p 사주풀이
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

### 98p 터널 진입 결과 도출
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

### 100p 연도, 월에 따른 마지막 날 계산
~~~c
#include <stdio.h>

int main(void) {
  int y, m, r1, r2, r3;
  printf("연도와 월을 입력하세요 (y m) :\n");
  scanf("%d %d",&y, &m);
  if(m==1||m==3||m==5||m==7||m==8||m==10||m==12)
    printf("31");

  else if(m==2){
  if(y%4+y%100!=0||y%400==0)
    printf("29");
  else
    printf("28");
  }
    
  else
    printf("30");
  
  return 0;
}
~~~

### 102p 30분전 시간 계산
~~~c
#include <stdio.h>

int main(void) {
  int h, m;
  printf("시간을 입력하세요 (h m) : \n");
  scanf("%d %d", &h, &m);
  if(m<30)
    if(h==0)
      printf("%d시 %d분의 30분전은 %d시 %d",h,m,23,60+m-30);
    else
      printf("%d시 %d분의 30분전은 %d시 %d",h,m,h-1,59+m-30);
  else
    printf("%d시 %d분의 30분전은 %d시 %d",h,m,h-1,m-30);
  return 0;
}
~~~

### 104p 책 구입
~~~c
#include <stdio.h>

int main(void) {
  int money, remain, book=15000;
  printf("책의 가격은 15000원입니다.");
  printf("당신이 가진 돈은 얼마입니까? : \n");
  scanf("%d", &money);
  if(money>book){
    remain = money-book;
    printf("책을 구입하였습니다. 이제 남은 용돈은  %d원입니다.",remain);
  }
  else{
    printf("책을 구입하지 못했습니다.");
  }
  return 0;
}
~~~

### 105p switch case
~~~c
#include <stdio.h>

int main(void) {
  int a;
  printf("a를 입력하세요 : ");
  scanf("%d", &a);
  switch(a)
  {
    case 1 : printf("1st");break;
    case 2 : printf("2nd");break;
    case 3 : printf("3rd");break;
    default: break;
  }
  return 0;
}
~~~

### 도어락
~~~c
#include <stdio.h>

int main(void) {
  int a, b, pw=24680;
  char c, ic = 'c';
  double d, fp = 1.2345678;
  printf("장치 선택: ");
  scanf("%d", &a);
  switch(a){
    case 1:
      printf("IC 카드: ");
      scanf(" %c", &c);
      break;
    case 2:
      printf("비밀번호: ");
      scanf("%d",&b);
      break;
    default:
      printf("지문: ");
      scanf("%lf",&d);
    break;
  if(b==24680||c=='c' || d==1.2345678)
    printf("잠금해제");
  else
    printf("오류발생");
  }
  return 0;
}
~~~
# 혹은
~~~c
#include <stdio.h>

int main(void) {
  int a, pw_insert, pw=24680;
  char ic_insert, ic = 'c';
  double fp_insert, fp = 1.2345678;
  printf("장치 선택 (1. IC 카드, 2. 비밀번호, 3. 지문) : \n");
  scanf("%d", &a);
  if (a==1){
    printf("IC 카드를 입력하세요 : \n");
    scanf("%s", &ic_insert);
  }
  else if(a==2){
    printf("비밀번호를 입력하세요 : \n");
    scanf("%d",&pw_insert);
  }else{
    printf("지문을 입력하세요 : \n");
    scanf("%lf",&fp_insert);
  }
  if (fp==fp_insert||ic==ic_insert||pw==pw_insert)
    printf("문 열렸다, 들어갈 때 문 잘 닫고");
  else
    printf("다rrrrrrrrr릭 다rrrrrrrrr릭");
  return 0;
}
~~~
### 가위바위보
~~~c
#include <stdio.h>
int main(void) {
 char def, choice;
 def='r';
 ///def='p'
 ///def='s'
 printf("입력(가위:s, 바위:r, 보:p): \n");
 scanf("%c", &choice);
 if(choice==def)
   printf("비겼다.");
 else if((def=='r' && choice=='p')||(def=='p' && choice=='s')||(def=='s' && choice=='r'))
   printf("이겼다.");
 else
   printf("졌다.");
 return 0;
}
~~~
