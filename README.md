# Study

요약
Javap -v Demonstrate -> byte code가 나온다.
JRE - 실행할 환경을 만드는 것
Java Compiler(Javac) - 개발 할 때 사용
Git token - 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
.Zshrc을 통해 정보를 알수 있음.
- Mvn clean 을 그냥 하는 것 보다 mvn clean package
- 를 해주는 것이 훨씬 더 좋다.
- 함수 쓰는 방법 을 모를 때 
- 1. Cmd + B
- 2. Cmd + fn + f12 후 하고 싶은 함수 찾은 뒤 읽어 본 뒤에 추가 하면 됨.
- 

9/5 (화)
JVM - java virtual machine에 대해 공부하기
for문에서 필요한 것
1. 종료조건

9/6 (수)

1. Collection Framework - stack, queue, hash map 등이 모여있는 것.
2. Adhoc -> 이것을 위해 즉 특별한 목적을 위해서 student를 받는 이유는 department의 값을 알기 위해서 이 방식이 adhoc방식
3. 

9/12 (화)
공부하는 방법
1. Java oracle 이용해서 공부

Javac -> 컴퓨터에서 직접 실행할 수 있는 일련의 명령으로 변환하는 프로그램 컴파일러이다.
Java 바이트 코드라는 코드를 생성한다.
Editor(Inteli J) -> java source code 작성 -> Compiler(Javac) -> 
Libraries - Class file(컴파일러로 만들어진 클래스 파일) ->
java virtual machine(바이트 코드 해석기) -> 프로그램이 실행됨.

코드의 가독성(readability)을 위해 -> 들여쓰기(indentation)은 중요하다.
System.out -> PrintStream의 instance of the predefined

Invocation object -> 호출 객체
Object.MethodName(parameter); == System.out.println(“Ciao”);
System.out -> 호출 객체 이다. 
Println(…) -> 호출된 메서드.
Ciao-> 전달된 parameter(매개변수)이다.

Entity -> 2차원 Table 자체를 의미한다.
객체는 프로그램에 의해 조작될 수 있는 Entity이다.
-> 무분별한 setter사용 지양(언제 어디서 변경되는지 파악하기 어려움)

객체 - class of instance(속성) 그리고 클래스에 속한다.

Overloading -> method의 이름은 같지만 signature가 다른 경우를 뜻한다.
Ex) (new 내가 만든)substring method in the class String

Parameter -> method가 수행해야 하는 작업을 실현하는데 필요한 값
Ex) println(“Ciao”)는 System.out 이라는 invocation object에서 사용할 수 있는 method 이다. 여기서 println을 할 때 ciao라는 parameter 값이 필요하다.

또 다른 경우인 xxx.concat(“YYY”);
Xxx : invocation object
YYY: parameter
이런 경우 처럼 다른 메서드를 호출하여 얻어야 할 수도 있다.

Static method
ClassName.method(parameter);
ClassName : method 가 속한 class
Method : 호출된 메서드
- Invocation object를 지정할 필요 없이 매개변수만 지정

Variables
만약에 str.toUpperCase()가 두번 사용 되는 경우를 방지하기 위해 이 표현식을 variable에 저장하고 재사용 할 수 있다.
Ex) String line = str.toUpperCase();

각 변수에는 연관된 메모리 위치가 있다.
메모리 위치의 크기는 변수 유형에 따라 다르다. Ex) Integer, long, short …
자바에서는 메모리 위치의 주소를 알 수 있는 방법이 없다.

-> 프로그램 실행 중에 변수는 이름 유형 주소는 변경 할 수 없지만, 값은 변경할 수 있다.

변수 초기화 -> 변수에 할당할 초기 값을 지정하는 것을 의미

초기화 되지 않은 변수에는 정의된 값이 없으므로 해당 값이 할당 될 때 까지 사용 X
초기화 되지 않은 변수에는 값이 없으며 심지어 null도 없습니다.

Invocation of Construction
- 생성자의 이름은 클래스 이름과 같다.
- 특정 클래스에는 parameter의 수, 유형이 다른 여러 생성장가 있을 수 있다.
- 생성자를 호출하면 생성자가 속한 클래스의 새 개체가 생성되고 생성된 개체에 대한 참조가 반환된다.

StringBuffer()
- 문자가 없고 character타입으로 16인 문자열 버퍼 생성
- String은 불변 객체이다. 그래서 자신의 상태를 바꿀 수 없고 바꾸고 싶으면 코드 내부애서 new StringBuffer를 반복하게 되므로 메모리에 효과적이지 않아서 사용한다.
- 가변 객체 : 가변 객체는 자신의 상태를 수정할 수 있어야 한다.
- 

09/13 (수)

Modularization(모듈화)

프로그램은 모듈이라고 불리는 자율적인 부분으로 구성되어야 한다.
다양한 모듈은 정확한 관계를 통해 서로 연관되어있다.

모듈이란 서로 밀접하게 연관된 패키지들과 리소스들의 그룹이다.

특징
- Service exported : 메서드가 무엇을 인식하는지
- An interface : 해당 서비스를 내보내는 방식 -> 메서드 헤더
- Imported services : 클라이언트가 사용하는 모듈의 서비스
- An internal structure : 모듈이 어떻게 구현되는지

모듈화를 사용하면 할 수 있는 것

- 요청된 문제를 해결하는 데 필요한 모듈을 정의한다.
- 우리는 이러한 모듈이 어떻게 관련되어 있는지 정의 한다.
- 각 모듈을 다른 모듈과 독립적으로 개발한다.

-> 이러한 방식으로 프로그램 처리를 단순화 할 수 있고 품질을 향상 시킬 수 있다.
 - readability of the program
 - extensibility (확장성)
 - reusability of parts (다양한 목적으로 프로그램 일부 재사용)

Abstraction

모듈화는 추상화 개념과 밀접하게 결합되어 있다.

유형
- Abstraction of operations : 어떻게 해야 할지가 아닌 무엇을 수행해야 하는지에 집중
	-> method를 통해 실현
- Abstraction on object : 
	1. 유사한 객체(동일한 속성을 가진 객체)를 클래스로 그룹화한다.
	 ex) 소나타, 아반떼, 토레스 -> 차 (그룹화)
	2. 우리는 객체의 관련 속성, 특히 객체가 지원하는 작업을 설정

Static method (정적 메서드)

- 정적 메서드는 호출 객체가 없는 메서드(클래스에 정의됨) 입니다.

Public static resultType methodName(formal parameter)
Static : 메서드가 정적임을 나타냄.
resultType : 반화한 결과의 탑입을 정해주는 것을 나타냄.

- 반환된 결과는 메소드에서 호출된 값이다.

메서드 호출에는 메서드 인수로 사용해야 하는 formal parameter가 포함된다. 
이러한 parameter를 메서드 정의 헤더에 나타나는 formal parameter와 구별하기 위해 actual parameter 라 한다.

public static String duplicate(String pf) { <- formal parameter
        return pf + ", " + pf;
    }
    public static void main(String[] args) {
        String s;
        s = duplicate("pippo"+ "&" + "toplino"); <- actual parameter
        System.out.println(s); 
    }

1. formal parameter 가  "pippo"+ "&" + "toplino” 문자열을 나타내는 객체에 대한 참조로 초기화 된다.
2. return을 통해 String 값을 반환한다.
3. Formal parameter와 local variable에 대한 메모리가 해제된다.  -> formal parameter에 해당하는 메모리 위치가 해제 됩니다.
4. 이제 실행은 메서드 호출에 의해 멈춘 지점부터 계속된다.

Local variable 
 메소드 내의 있는 변수를 local variable이라 한다.
- Scope (범위) : 지역 변수의 범위(int형)
- lifetime (수명) : 다음 메서드가 호출되기 전까지 유지된다.
- 

Method Overloading
- 메서드 이름이 같은 두 개의 메서드는 존재 할 수 없다. 하지만 파라미터의 값이 다르다면 사용할 수 있다 -> 메서드 오버로딩이라 한다.

Abstraction on objects

- 유사한 객체를 클래스로 그룹화한다.
- 객체가 하는 작업과 관련된 속성을 설정한다.(이것을 위해 추상화한다.)

Instance Variable(인스턴스 변수)
- 클래스 내부의 있는 static이 들어가지 않은 field variable이다.
Instance Method
- 클래스의 객체에 대해 호출되어 작업을 수행 할 수 있다.

Data field : 객체의 내부 구조를 나타내는데 사용된다.
Operation field : 클래스 기능을 구현하는데 사용.

Rules for accessing the field of a class

- 클라이언트가 관심을 갖는 클래스 기능에 해당하는 메서드는 public으로 선언
- 인스턴스 변수와 보조 메서드, 즉 메서드를 구현하는데 도움이 되는 메서드는 private로 선언
- 요약 : 관심을 갖는 클래스는 public 관심을 갖지않는 인스턴스 변수 및 보조 메서드는 private로 설정하여 클래스 내부에서만 볼 수 있게 만듦.

Instance Variable lifetime

- 변수가 속한 객체의 수명과 일치한다. 
- 객체가 생성되는 순간 생성.
- 참조가 없으면 Gabage Collector를 통해 자동으로 삭제한다.

This -> invocation Object이다.

인스턴스 변수와 지역변수를 구별하기 위해 사용.

Static Method 사용 할 때 
- 변화를 가정하지 않는다.
- 메소드가 인스턴스 변수를 사용하지 않는다.
- 인스턴스 생성에 의존하지 않는다.
- 메소드가 공유되고 있다면, 정적 메소드로 추출해낼 수 있다.
- 메소드가 변화되지 않고, 오버라이딩 되지 않는다.

Inheritance
- 이미 존재하는 클래스와 동일한 속성을 가지지만 새 기능을 추가하려는 클래스를 정의 하는 것 이다.
- Student -> Person의 하위 클래스이다.
- Person -> Student의 슈퍼 클래스이다.
- 슈퍼 클래스의 모든 메서드와 모든 인스턴스 변수를 상속할 수있다. -> 슈퍼 클래스의 메서드를 사용 할 수 있다.
- 반대로 슈퍼클래스는 하위 클래스의 메서드는 사용할 수 없다.
- Student 객체를 사용하는 파라미터가 있을 경우 이 때는 슈퍼클래스를 actual parameter로 설정 불가능하다.

Method Overriding
- 슈퍼클래스 메서드와 정확히 동일한 시그니쳐를 갖는 메서드를 서브클래스에 정의 할 때 메소드의 오버라이딩이라 한다.
- Polymorphism(다형성)이 생긴다.
- 정적 메서드는 오버라이딩을 할 수 없다.

Late binding
1. 바인딩 -> 각종 값들이 확정되어 더 이상 변경할 수 없는 상태가 되는 것
2. Late binding은 객체를 나타내는 유형의 메서드가 아닌 객체가 속한 클래스를 기반으로 메서드가 사용 되는 것
3. toString()은 late binding을 기반으로 이루어진다. 
 	-> toString을 나타내는 유형 - Object
	-> 객체가 속한 클래스 - Person
	-> 그럼 person에서 Override(재정의)한 toString()의 기능이 사용된다.

9/14 (목)

Data type
- Domain (정수, 실수) : 컴퓨터 메모리에 표시 될 수 있는 가능한 값의 집합
- 연산(sum, multiply) : 기본 연산을 수행 할 수 있게 해주는 프로그래밍 언어의 연산자
- 상수를 나타내는 상수 집합.(23) : 기본 데이터 유형의 값을 정의하는 언어 기호(10, 3.14, ‘A’, true 등)

자바 기본 데이터 유형
- Int, long, short, byte, float, double -> 정수와 실수 표현
- 숫자가 아닌 기본 데이터 유형 2가지  char, boolean이다.
- 

9/15 (금)
- Initialize : 변수 초기화 -> 최초로 할당하는 것.
- Allocation : 변수 바꾸는 할당.
- Declare : 변수를 선언하는 것. -> 이유는 : 값을 저장하는 공간을 확보 하겠다는 의미이다.
- Assignment : 변수를 할당 ex) x = 7
- Side effect(부수작용) -> 값이 allocation이 일어날 때마다 작용하는 것. 
- 또는 reference type에서 두 개의 객체의 값이 의도치 않기 동시에 allocation이 일어날 때를 말한다.
- literal(상수) 값을 한 번 저장하면 변경할 수 없는 변수로 정의 -> final
- Expression :  값을 기술한 것. -> 하나의 값으로 치환된다.
- Statemetn : 하나의 동작을 기술한 것.
- Arithmetic : 연산 +, -, / , * …
- Expression 내부에 statement가 2개 이상 들어가서는 안된다.
- Constant : 변하지 않는 변수 또는
-  참조변수 메모리의 주소값이 변하지 않는다라는 의미 
- -> 그 주소가 reference하는 데이터 들까지 constant라는 의미는 아니다.
- Ex) final Test t1 = new Test(); 
-       t1 = new Test(); -> 주소값이 변할 수 없음!
- T1.num = 10; -> 이 경우는 가능하다.
- Literal : 변수에 넣는 변하지 않는 데이터(불변 데이터)
- Boolean, char, double, long, int
- 하지만 instance안의 값들은 literal이라 할 수 없다.
- 동적으로 사용되며 값이 언제 바뀔지 모르기 때문이다.
- Ex) final int a = 1; 
- a -> constant, 1 -> literal
- 요약 : constant -> 메모리 위치를 변경 할 수 없다.
- Literal -> 메모리 위치 안의 값을 의미한다.
- Numeric data 
- Approximate type : 부동 소수점 data.type이 포함된다.
- Exact type : 정수 데이터 유형과 십진 데이터 유형이 포함된다.
- Primitive type : 변수 값은 primitiver type 자체의 값이다.
- Reference type : 변수 값은 객체에 대한 참조이며 객체 자체가 아니다.
- Parameter passing 2가지
- 1. Call by value(값으로 전달)
- Actually parameter에서 전달된 값은 호출 수신자 메서드의 formal parameter로 들어가게 된다. 여기서 들어간 parameter는 그저 actual parameter의 복제복이다. 그래서 메소드에서 수행된 수정은 actual parameter에 영향을 끼치지 않는다.
- 2. Call by reference(참조로 전달)
- parameter가 참조에 의해 전달 되는 경우 actual parameter와 formal parameter는 같은 객체를 가르키게 된다. 그래서 메소드에서 formal parameter의 값을 수정하게 되면 해당하는 객체의 값이 바뀌게 된다.
- wrapping class는 primitive type을 객체로 만들 수 있는 박싱 기능이 잇으며 그 반대의 기능을 할 수 있는 unBoxing 기능도 가지고 있다.
- Operator : 연산자
- Specific interval : primitive data type의 크기(특정 간격)
- Integer Cycle
- Integer.Max_VALUE + 1 == Integer.MIN_VALUE
- final을 declare(선언)하여 constant를 만들어서 사용한다.
- Decimal digit : 0,1,2,3,4,5,6 …
- 만약 integer type 과 floating point와 계산을 해야한다면 값은 floating point type의 값으로 나오게 된다.
- Int a 와 float b 값을 int 형으로 표현 하고 싶다면 b를 conversion 해줘야 한다. -> (int)b 이런식으로
- Loss of precision : 어떠한 작업을 수행할 때 정밀도 손실에 의해 결과가 영향 받을 수 있다. 
- Ex) int a = (int)3.75 -> a = 3으로 된다. 0.75가 손실 됨.
- Boolean algebra : 이진변수를 사용한 논리적 값에 대한 연산을 다루는 수학.
- Floating point number 비교 : 0이 나오더라도 0이랑 비교해보면 false의 값이 출력된다.
- 그래서 == 을 해서 비교할 수는 없다. 
- 그럼 비교하려면 절댓값x-y와 eps(가장 작은 수) 를 비교하여 eps가 더 크거나 같으면 x와 y는 비슷한 수를 가지고 있다는 것을 알 수 있습니다.
- Predicate : 결과 값이 boolean type인 것을 말한다.
- 다른 타입의 연산자들에서의 우선 순위
1. !(not)
2. Arithmetic operator(산술 연산자)
3. Relational oparator(관계 인산자) >, <, ==, …
4. Logical (&&, ||)

9/16 (토)
Represent : 표현하다.

9/17(일)
객체지향 프로그래밍 : 현실 세계의 사물같은 객체를 만들고, 객체에서 필요한 특징들을 뽑아 프로그래밍을 수행. 
여기서 특징은 field, method 예를 들어 키보드의 버튼을 누른다. -> 이러한 행동들을 method로 표현. 각가의 상태를 변수로 표현한다.
4가지 특징이 있다.
1. 추상화(abstraction) 
2. 캡슐화()
3. 상속성(inheritance)
4. 다형성(polymolyphism)
5. 

Realize - 실체화 하다.
- 인터페이스를 상속 받아 자식클래스에서 재사용
- 부모클래스의 은닉화 선언된 필드 또는 메소드는 상속되지만 접근은 불가능
- 부모 인스턴스 생성 후 자식 인스턴스 생성

메소드가 호출되고 끝나면  메모리에 있던 formal parameter와 local variable는 모두 사라집니다.

Activate record : procedure가 한 번 수행되기 위해 필요한 정보들은 기억 장소의 연속 블록을 사용하여 관리하게 되는데, 이러한 연속 블록

Procedure : 컴퓨터 프로그래밍에서 동일한 목적에 사용하는 일련의 명령문들을 모아놓은 것이다. 즉 프로그래밍에서 루틴이나,  서브루틴 및 함수와 같은 뜻이다.

9/18(월)
Access modifier : 접근 제어자

Visibility : 가시성
- 클래스와 클래스 멤버인 멤버 필드와 메소드의 사용범위를 결정하는 것이다.
- 한 클래스의 멤버필드와 메소드에 대한 다른 클랫의 접근 여부를 접근제어자로 제어하는 것이다.
- 

Selection operator - person.getperson()에서 “.”역할이 selector operation이다.

JRE - JDK를 사용하여 작성된 java 코드를 JVM에서 이를 실행하는 데 필요한 필수 라이브러리와 결합한 후 결과 프로그램을 실행하는 JVM의 인스턴스를 작성한다.

Argument - 메소드 호출시 전달 되는 값.

Standard constructor : constructor without argument(argument가 없는 생성자)

설계 방법론(design methology)
- 클래스의 사용 예제를 고려하고 그에 따라 클라이언트 코드를 작성하는 것이 중요하며, 클래스의 공개 메소드 내용을 구체화하거나 보조 메소드를 도입하기 전에도 클라이언트를 먼저 생각하고 구현할 수 있다는 점을 강조한다.
- Skeleton of the class : 클래싀 기본 구조, 클래스의 뼈대 또는 초기 버전을 생성하는 것을 나타낸다.
1. Public interface : 클래스 이름은 해당 클래스가 나타내는 객체 또는 개념을 의미 있기 표현해야 한다.
2. Representation for the objects : 객체를 나타내기 위한 클래스 디자인 예제를 의미. -> 클래스는 객체의 틀이며, 객체를 표현하고 다루기 위한 구조를 제공한다. -> 객체를 어떻게 표현하고 다루는지를 나타낸다.
3. Realization of the methods : 클래스는 데이터와 메서드를 포함한다 이 메소드를이 어떻게 동작해야 하는지를 구체화하는 과정이다.
4. A client : 클라이언트란 해당 클래스를 사용하는 코드 또는 프로그램의 일부를 나타낸다. 이것은 클래스의 인스턴스를 생성하고 클래스의 메소드를 호출하여 해당 클래스를 실제로 활용하는 부분을 나타냅니다.

문제를 해결해야 할 때, 우리는 어떤 조건이 true인지 false인지에 따라 다른 행동을 하는 것에 관심이 있다.

Composite statement : 여러 하위 문장이나 statement 결합된 하나의 문장을 나타낸다. 
- If - else : 두 개의 대안 중 하나를 고르는 것.
- Switch : 여러 대안 중 하나를 고르는 것.
If - else 문의 조건은 boolean type의 임의의 식일 수 있다. -> predicate이다.

If statement scope
- 블록 내에서 declare variable은 그 블록의 하위 블록에서는 사용이 가능하지만 그 블록의 외부에서는 사용이 불가능하다.
- 

if문 사용
- 조건이 지정된 순서가 중요하다.
- 마지막에 else 문에는 굳이 condition을 쓸 필요가 없다. 어차피 else문의 conditon이 true이기 때문
- 각각의 else는 바로 앞의 if문을 가르킨다. 즉 if문과 그에 대응하는 else문은 서로 쌍을 이룬다.



Complex condition : 조건식의 복잡성 -> shortcut evaluation이다.

1. Shortcut evaluation : 첫번째 인수가 값을 결정하기에 충분하지 않은 경우에만 두번 째 인수가 평가되는 일부 프로그래밍 언어의 일부 논리 연산의 계산이다.
2. Eliminating the conjunction == && -> && 양 옆의 조건들이 모두 true여야 하는 것이다.
3. Eliminating the disjunction = || -> || 양 옆의 조건들 중 하나의 조건만 만족해도 된다.

Conditional Expression
- (A > b) ? A : b; -> condition이 참일시 A의 값을 뽑아내고
- False 이면 : 뒤의 값을 얻는다.

Equality between strings(문자열 간의 동일성)
- 문자열을 instance 하여 두 개의 string값을 비교할 때 ==을 사용하면 false가 나온다. 
- 이유 : string 객체가 생성되면 heap영역에 생기게 되고 또 새로운 string 객체를 생성하게 되면 서로 다른 주소를 참조하게 된다. ==은 여기서 주소값을 비교하기 때문에 계속 false가 나온다.
- 해결방법 : 문자열.equals(문자열)을 해야 true값이 출력된다.

Lexicographic comparison
- 문자열 또는 다른 순서 있는 요소들을 알파벳적인 순서 또는 문자들의 순서를 기반으로 비교하는 방법을 의미한다.
- compareTo method를 사용한다.

compareTo method
1. 비교대상이 문자열이 포함되어 있을 경우 만약에 abcd.compareTo(ab); 라 하면 기준 값인 abcd 와 ab를 비교하게 되는데 여기서 기준값에 비교대상이 포함되어있을경우 서로의 문자열 길이의 차이값을 리턴해준다. 그래서 2가 출력될 것이다.
2. 비교대상과 전혀 다른 문자열이 경우 - 비교가 불가능한 지점의 각 문자열의 아스키값을 기준으로 비교를 해준다. Abcd.compareTo(c) 인 경우 처음 a = 97 c = 99이다. 여기서 아스키 코드를 빼면 -2가 출력되어 다르다는 것을 알 수 있다.

객체를 참조하지 않는 객체에 대한 참조 타입 변수의 값은 null이다.

null과 비교하기 위해서는 equals를 사용하지 않고 ==을 사용해야 한다.

Iterator -> guaba	활용해서 공부 
Linkedlist -> master.


람다 스트림 스레드 -> 네트워킹

11/19 -> 코테 날짜

코테는 점수 위주 평가 -> 모르는 거는 바로 넘겨야함. 맞춰야함.

웹 브라우저에서 source안에서 모든 파일에서 검색하고 싶을 때 :
Cmd + option + F를 누르면 된다.
