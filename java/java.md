# 자바의 특징
* 배우기 쉬운 객체지향 언어
* 자동 메모리 관리
  * 가비지 컬렉터(GC) : 메모리를 알아서 정리해줌 프로그램을 작성하기 매우 편리
* 멀티 쓰레드를 지원 : 동시작업 지원
* 풍부한 라이브러리로 쉽게 개발가능
  * 프로그램을 작성할때 필요한 코드들이 많다.
* 운영체제의 독립
  * 자바 가상 머신(JVM)

# 자바의 개발도구
* JDK(Java Development Kit, 자바 개발도구)
* JDK 다운로드
  * https://www.oracle.com/kr/java/technologies/javase-jdk11-downloads.html
# Java API 문서
* Java API
  * Java로 프로그램을 만드는데 필요한 주요 기능을 미리 만들어서 제공
* Java API 문서
  * Java API가 제공하는 기능에 대한 상세한 정보제공 (html파일)
  * Java API = Java의 사전
* Java API 다운로드
  * https://www.oracle.com/java/technologies/javase-jdk8-doc-downloads.html

<br/>

# 자바프로그램 작성 (1)
* cd ___ : 현재 디렉토리에서 다른 디렉토리로 이동할때.
* dir : 현재 폴더에 있는 파일을 모두 보여줌.
* type ___ : 파일에 내용을 알려줌
  * 이진법 파일(Hello.class) : 사람이 알아볼 수 없는 파일 내용
  * 텍스트 파일(Hello.java) : 사람이 알아볼 수 있는 파일 내용
<br/>

* javac.exe(자바 컴파일러) : 사람이 작성한 문장을 기계어로 번역
  * 소스파일(.java)을 클래스 파일(.class)로 변환.
* java.exe(자바 인터프리터) : 자바 프로그램(클래스 파일)을 실행
<br/>

* ## 소스파일의 구성 - 클래스(class) 와 메서드(main)
  * 클래스(class) - 자바 프로그램의 단위
    * 자바 프로그램은 클래스들로 구성
<br/>

    class 클래스 이름 {      <---클래스의 시작
    <br/>
    }     <---클래스의 끝 
<br/>

  * 메서드(main) - 자바 프로그램의 시작점. 이 메서드 없이 실행 불가
<br/>

    class 클래스 이름 {
    public static void main(String[] args) {     <---메서드의 시작
    }    <---메서드의 끝
    }
<br/>

# 본격!! 자바 이클립스 사용하기
* 자바 단축키
  *  ctrl + shift + L : 단축키 목록 보기 
  *  trl + S : 저장
  *  ctrl + F11 : 실행
  *  trl + A : 전체 선택
  *  ctrl + D : 한 줄 삭제
  *  trl + delete : 다음 단어 삭제
  *  ctrl + +, - 또는 ctrl + shift +, - : 편집창 폰트 크기
  *  ctrl + space : 자동 완성
  *  alt + ctrl + shift + ⇧, ⇩ : 행 복사(여러 행 가능)

* 주석달기의 주의점
  *  문자열을 의미하는 큰따옴표(“”) 안에 주석이 있을 때는 주석이 아닌 문자열로 인식된다는 것이다.
```
class Hello
{
 public static void main(String[] args) 
 { 
 System.out.println("Hello, /* 이것은 주석 아님 */ world."); 
 System.out.println("Hello, world. // 이것도 주석 아님"); 
 }
}
```
* 화면에 글자 출력
  * 화면에 글자를 출력할 때는 System.out.print(출력하고자하는 내용 입력)
  * “ ” 안에 넣은 내용은 글자로 간주 (단어로 입력됨)
```
System.out.print("Hello, world"); // 화면에 Hello, world를 출력
System.out.print(3+5); // 화면에 8을 출력
System.out.print("3+5"); // 화면에 3+5를 출력
```

* System.out.print( ) 과 System.out.println( ) 의 차이
```
System.out.print() 괄호 안의 내용을 출력하고 줄바꿈을 하지 않는다.
System.out.println() 괄호 안의 내용을 출력하고 줄바꿈을 한다.
```

# 변수

* 변수란?
  * 하나의 값을 저장할 수 있는 저장공간
* 변수를 선언하는 방법
  * 변수타입 변수이름; // 반드시 끝에는 ";"를 붙여야 한다!!
```
int x; // 정수(integer)를 저장하기 위한 변수 x를 선언
x = 5; // 변수 x에 5를 저장
```

* 변수의 타입
  * 정수 : int
  * 실수 : pi
  * 문자 : ch
  * 문자열 : str
```
int x = 100; // 정수(integer)를 저장할 변수의 타입은 int로 한다.
double pi = 3.14; // 실수를 저장할 변수의 타입은 double로 한다.
char ch = 'a'; // 문자(1개)를 저장할 변수의 타입은 char로 한다.
String str = "abc"; // 여러 문자(0~n개)를 저장할 변수의 타입은 String으로 한다
```
  * ### 정수
    * `int` : 20억 이하의 정수
    * `long` : 20억 초과의 정수
  * ### 실수
    * `float` : 오차없는 7자리 실수
    * `double` : 15 자리 실수
  * ### boolean 변수
    * true or false 만 입력 가능


# 상수와 리터럴

* 상수 : 변수와 마찬가지로 ‘값을 저장할 수 있는 공간’이지만, 변수와 달리 한번 
값을 저장하면 다른 값으로 변경할 수 없다.
  * 상수에 값이 저장된 후에는 상수의 값을 변경하는 것이 허용되지 않는다.
  * 상수를 선언하는 방법은 변수의 타입 앞에 키워드 ‘final’을 붙여준다.
 
```
final int MAX_VALUE; // 정수형 상수 MAX_VALUE를 선언 
MAX_VALUE = 100; // OK. 상수에 처음으로 값 저장 
MAX_VALUE = 200; // 에러. 상수에 저장된 값을 변경할 수 없음.
```
* 리터럴 : 그 자체로 값을 의미하는 것
  * 우리가 흔히 아는 상수 대신 프로그래밍언어 에서는 상수 대신 '리터럴'이라 한다.
```
★정리
변수 (variable) 하나의 값을 저장하기 위한 공간
상수 (constant) 값을 한번만 저장할 수 있는 공간
리터럴 (literal) 그 자체로 값을 의미하는 것
```

# 리터럴의 타입과 접미사

* 타입 : 논리형, 정수형, 실수형, 문자형, 문자열
  * 접미사
    * 정수형 : long 타입의 리터럴에 접미사 "l 또는 L"을 붙인다. ---> long 타입 : L, l
    * 실수형 : float타입 리터럴에는 ‘f’를, double타입 리터럴에는 ‘d’를 붙인다. ---> float타입 : 'f' , double타입 : ‘d’
    * ※ 정수형에서는 int가 기본 자료형인 것처럼 실수형에서는 double이 기본 자료형이라서 접미사 ‘d’는 생략이 가능하다.
        #### 접미사 f와 L 두 개는 꼭 기억하자!!!

```
long big = 100_000_000_000L; // long big = 100000000000L; 
long hex = 0xFFFF_FFFF_FFFF_FFFFL; // long hex = 0xFFFFFFFFFFFFFFFFL;
float pi = 3.14f; // 접미사 f 대신 F를 사용해도 된다. 생략불가
double rate = 1.618d; // 접미사 d 대신 D를 사용해도 된다. 생략가능
```

  * 진수 만들기
    * 10진수 : x__
    * 8진수 : 0__
    * 16진수 : 0x__
    * 2진수 : 0b__ 

```
int octNum = 010; // 8진수 10, 10진수로 8
int hexNum = 0x10; // 16진수 10, 10진수로 16
```

# 문자, 문자열 리터럴  주의사항
* 문자열 리터럴은 “ ” 안에 아무런 문자도 넣지 않는 것을 허용하며, 이를 빈 문자열(empty string)이라고 한다. 
* 그러나 문자 리터럴은 반드시 ‘’ 안에 하나의 문자가 있어야한다.
   #### 문자열은 "" 공백을 허용한다.
```
String str = ""; // OK. 내용이 없는 빈 문자열
char ch = ''; // 에러. '' 안에 반드시 하나의 문자가 필요
char ch = ' '; // OK. 공백 문자(blank)로 변수 ch를 초기화
7 + 7 + "" → 14 + "" → "14" + "" → "14"
"" + 7 + 7 → "7" + 7 → "7" + "7" → "77"
```

# 두 변수의 값 바꾸기

* 단순히 x의 값을 y에 저장하고, y의 값을 x에 저장해서는 원하는 결과를 얻을 수 없다.
* 두 컵에 담긴 내용물을 바꾸려면 빈 컵이 필요한 것처럼, 값을 임시로 저장할 변수가 하나 더 필요하다.
* 바로 ---> tmp

```
 int tmp; // 임시로 값을 저장하기 위한 변수(빈 컵 역할)
 tmp = x; // ① x의 값을 tmp에 저장
 x = y; // ② y의 값을 x에 저장
 y = tmp; // ③ tmp에 저장된 값을 y에 저장
 ```
 
 # 기본형과 참조형
 
* #### 기본형 (primitive type)
  *  논리형(boolean)
  *  문자형(char)
  *  정수형(byte, short, int, long)
  *  실수형(float, double)계산을 위한 실제 값을 저장한다. 
  *  모두 8개

* #### 참조형 (reference type)
  * 객체의 주소를 저장한다.
  * 8개의 기본형을 제외한 나머지 타입
  *  ex) string, system, today 
 
# 기본형의 종류와 크기

종류/크기 <br/>    1    2    4    6

논리형 <br/>    boolen 

문자형 <br/>

정수형 <br/>

실수형 <br/>
