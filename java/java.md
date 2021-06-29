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

* # 소스파일의 구성 - 클래스(class) 와 메서드(main)
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
