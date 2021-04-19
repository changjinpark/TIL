# JVM, JDK, JRE 이해하기

### 1. JVM이란 무엇인가?
자바 가상 머신(JVM)은 바이트 코드를 실행시킬 수 있는 프로세스.

java 소스 파일(*.java)을 컴파일러(javac)가 컴파일하면 바이트 코드(*.class)가 생성되고, 이 바이트 코드는 JVM으로 실행된다.

### 2. 왜 자바를 플랫폼에 독립적이라고 하는가?
컴파일한 바이트 코드는 Windows OS이던, Mac OS이던, Linux OS이던 운영체제에 설치된 JVM이 실행시킨다. OS의 종류와 상관 없이 바이트 코드를 동일하게 실행시킬 수 있어 플랫폼에 독립적이라고 한다.

### 3. JDK와 JRE의 차이점?
JDK(Java Development Kit): JRE + 개발 툴(javac 컴파일러 등)

JRE(Java Runtime Environment): JVM + 클래스 라이브러리
