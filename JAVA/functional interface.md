

# Lambda

### @FunctionalInterface
- 함수형 인터페이스는 추상 메서드가 오직 하나인 인터페이스를 의미
- 추상 메서드가 하나라는 뜻은 default method or static method는 여러개 존재해도 상관 없다는 뜻
- 해당 인터페이스가 함수형 인터페이스 조건에 맞는지 검사함
- 어노테이션이 없어도 함수형 인터페이스로 동작하고 사용하는데 문제는 없지만, 인터페이스 검증과 유지보수를 위해 붙여주는게 좋음

## 매개변수, 리턴값

### X, X

~~~java
@FunctionalInterface
interface JavaCoding {
    void nowCoding();
}

public class prac1 {
    public static void main(String[] args) {
        // 객체 선언
        JavaCoding jc;

        // {} 실행코드 뒤에 세미콜론(;)을 붙여야한다.
        jc = () -> {
            System.out.println("Rollin");
        };
        jc.nowCoding();

        // {} 실행코드가 1줄인경우 {} 생략가능

        jc = () -> System.out.println("Rollin2");
        jc.nowCoding();
    }
}
~~~

### O, X
~~~java
interface JavaCoding2 {
    void nowCoding2(String ddffdgdfgfd);
}

public class prac2 {
    public static void main(String[] args) {

        JavaCoding2 jc2;
        String str;

        jc2 = (a) -> {
            System.out.println(a + " Rolling in the deep"); // a가 매개변수 값
        };
        str = "하루가 멀다하고";
        jc2.nowCoding2(str);

        jc2 = a -> System.out.println(a + " 기다리고 있어요");
        jc2.nowCoding2("온종일 난 그대 생각에");
    }
}
~~~

### X, O
~~~java
interface Javacoding3 {
    String nowCoding3();
}

public class prac3 {
    public static void main(String[] args) {
        Javacoding3 jc;

        String str1 = "abc";
        String str2 = "bcc";
        String str3 = "ccc";

        jc = () -> { return str1; };
        System.out.println(jc.nowCoding3());

        jc = () -> { return str2; };
        System.out.println(jc.nowCoding3());

        // 실행코드가 return만 있는 경우 {}와 return문 생략가
        jc = () -> { return str3; };
        System.out.println(jc.nowCoding3());

    }

}
~~~


### O, O
~~~java
@FunctionalInterface
interface Javacoding4 {
    String nowCoding4(String s);
}

public class prac4 {
    public static void main(String[] args) {
        Javacoding4 jc;

        String str1 = " aaa";
        String str2 = " bbb";
        String str3 = " ccc";

        jc = (s) -> {
            return s + str1;
        };
        System.out.println(jc.nowCoding4("온통"));

        jc = (s) -> { return s + str2; };
        System.out.println(jc.nowCoding4("나도"));

        jc = (s) -> { return s + str3; };
        System.out.println(jc.nowCoding4("너무"));

    }
}
~~~

<img width="856" alt="스크린샷 2023-02-07 오후 7 07 50" src="https://user-images.githubusercontent.com/111875357/217215099-f49d1f89-f8bb-4c02-a9d4-bb1c435036be.png">

### 1) Consumer 함수적 인터페이스
- 역할 : 소비자, 매개값이 있고, 리턴값 없다
- 메서드 : accept()

XXXConsumer T - XXX 형태의 인자값을 받음

BiConsumer T,U - T, U 형태의 인자값 2개를 받음

ObjXXXConsumer T - T, XXX 형태의 인자값 2개를 받음

~~~java
import java.util.function.*;

public class ConsumerTest {

    Consumer<String> c1 = a -> System.out.println("입력값 : " + a);

    BiConsumer<String, Integer> c2 = (a, b) -> System.out.println("입력갑값1 : " + a + " 입력값 : " + b);

    IntConsumer c3 = a -> System.out.println("입력값 : " + a);

    DoubleConsumer c4 = a -> System.out.println("입력값 : " + a);

    LongConsumer c5 = a -> System.out.println("입력값 : " + a);

    ObjIntConsumer<Student> c6 = (a, b) -> System.out.println("이름 : " + a.name + " 숫자 : " + b);
    ObjDoubleConsumer<Student> c7 = (a, b) -> System.out.println("이름 : " + a.name + " 숫자 : " + b);

    ObjLongConsumer<Student> c8 = (a, b) -> System.out.println("이름 : " + a.name + " 숫자 : " + b);

    class Student {
        private String name;

        Student(String name) {
            this.name = name;
        }

        ;
    }

    public static void main(String[] args) {
        ConsumerTest test = new ConsumerTest();

        test.c1.accept("김유신"); // 그냥 값을 넣어주면 제네릭으로 스트링 넣어줘야함
        test.c2.accept("asdd", 12);
        test.c3.accept(12);
        test.c4.accept(13.45);
        test.c5.accept(1311341);

        Student student = test.new Student("이순신");
        test.c6.accept(student, 20);
        // c7나 c8이나 비슷
    }

}
~~~
  
### 2) Supplier 함수적 인터페이스
- 역할: 생산자, 매개값이 없고, 리턴값이 있다
- 메서드 : getXXX()

~~~java
import java.util.function.*;

public class SupplierTest {
    public static void main(String[] args) {
        String stringValue = "helloWorld";
        boolean booleanValue = true;
        double doubleValue = 12345.123;
        int intValue = 123;
        long longValue = 1234567;

        Supplier<String> supplier = () -> stringValue;
        BooleanSupplier booleanSup = () -> booleanValue;
        DoubleSupplier doubleup = () -> doubleValue;
        LongSupplier longup = () -> longValue;
        IntSupplier intup = () -> intValue;

        SupplierTest test = new SupplierTest();

        String s = supplier.get();
        System.out.println("String 값 : " + s);

        boolean b = booleanSup.getAsBoolean();
        System.out.println("boolean 값 : " + b);

        double d = doubleup.getAsDouble();
        System.out.println("double 값 : " + d);

        long l = longup.getAsLong();
        System.out.println("long 값 : " + l);

        int i = intup.getAsInt();
        System.out.println("int 값 : " + i);

    }
}
~~~
