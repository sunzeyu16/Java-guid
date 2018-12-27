
# Java 语法报错常见问题总结

1. 变量可能未初始化
错误提示：Abc.java:9: variable i might not have been initialized
                System.out.println(i);
中文说明：变量i可能没有赋值就使用了。
例子说明：
int i;
 System.out.println(i);
 
2. 变量重复定义
错误提示：Abc.java:9: i is already defined in main(java.lang.String[])
                int i = 2;
中文说明：变量重复定义了
例子说明：
 int i = 1;
 int i = 2;

3. 找不到符号：
Test6.java:26: cannot find symbol
symbol  : variable j
location: class Test6
   if(j < 0) {
     
4. 找不到类的错误
Main.java:4: cannot find symbol
symbol  : class T1
location: class Main
  T1 a = new T1();

5. 找不到方法的错误
Main.java:5: cannot find symbol
symbol  : method a()
location: class T
  a.a();
  
6. 找不到类
错误提示 Test.java:1: class Test1 is public, should be declared in a file named Test1.java
public class Test1 {
中文说明  test1是公共的，必须在文件中声明
例子说明  
 建一个文件为Test;在工具中打开这样写  public class Test11 {}; 就会报这个错误
 
7. 找不到这个类（类名跟文件名不一致）
NoClassDefFoundError: asa (wrong name: ASA)

8. 数组下标越界
java.lang.ArrayIndexOutOfBoundsException: 1
        at Test2.test2(Test2.java:30)
        at Test2.main(Test2.java:6)

9. 字符串下标越界
java.lang.StringIndexOutOfBoundsException: String index out of range: 6
        at java.lang.String.charAt(String.java:558)
        at Test2.test3(Test2.java:41)
        at Test2.main(Test2.java:7)
        
10. 空指向
Exception in thread "main" java.lang.NullPointerException
        at Next.main(Next.java:31)

11. 空返回值
错误提示 Test1.java:54: 'void' type not allowed here
   System.out.println(a5.deleteOnExit());
中文说明；此处不允许使用void返回值
例子说明  如果声明一个void的方法，那就不能直接输出来
  Public static void edit() {}
System.out.println(Test.edit());

12. 缺少返回值
asa.java:8: missing return statement
 int fan(){}
                  ^
1 error

13. 没有返回值的方法中不需要返回值
asa.java:10: cannot return a value from method whose result type is void
   return a;
                        ^
1 error

14. 引用的方法入参不对
Next.java:66: cannot find symbol
symbol  : method createTempFile(java.lang.String,java.lang.String,java.lang.String)
location: class java.io.File
   File ll = f.createTempFile("let","java","aaa");

15. 缺少形参
 del() in sms.service.Service cannot be applied to (int)
 
16. 无效的方法声明(需要返回类型)
    
    invalid method declaration; return type required
            public byteValue(){
          
17. 要求传入的是数组，却传入了字符串
array required, but java.lang.String found
                    ^
18. 找不到构造方法
    Main.java:4: cannot find symbol
    symbol  : constructor T()
    location: class T
    new T();

19. 数字格式化异常                                                   
    Exception in thread "main" java.lang.NumberFormatException: null 20. .不兼容的类型
    错误提示Test1.java:41: incompatible types
    found   : java.lang.String[]
    required: java.io.File[]
    File [] a3 = a11.list()；
    中文说明 不兼容的类型
    
20. 非静态方法不能在静态上下文中引用
    non-static method cannot be referenced from a static context
  
21. 不是静态方法而用静态方式调用（类名。方法）
    Main.java:5: non-static method fun1() cannot be referenced from a static context
                           Test.fun1();

22. 静态访问非静态（变量）
    Test.java:5: non-static variable a cannot be referenced from a static context
        a = 1000; 
        
23. 静态访问非静态（方法）
    Test.java:6: non-static method fun1() cannot be referenced from a static context
            fun1();                    // 静态的不能调用非静   
            
24. continue outside of  loop   (将continue放在for循环外的时候出现的错误报告)

25. illegal start of expression  违反规则的表达（将for循环中第二表达放置于for循环外或内部时出现的错误报告）

26. asa.java:6: unreachable statement     
    不能到达的语句（语句放于continue或break后出
    现不能到达，及continue和break后不能有语句）

27. break置于循环语句外
    asa.java:8: break outside switch or loop
     break;
            ^
1 error

28. 标识符错误（标识符不合法）；
    asa.java:2: <identifier> expected
     int %%;
                ^
    1 error

29. 没找到方法体，或声明为抽象的（方法）
    MyAbstract.java:6: missing method body, or declare abstract

30. 这个类不是抽象类    或者没有覆盖  重写方法fun1()   有抽象的方法的就必须是抽象类
    MyAbstract.java:1: MyAdstract is not abstract and does not override abstract method fun1() in MyAdstract

31. Myabstract 它是属于抽象类的，不能产生对象。
    3.Main.java:6: Myabstract is abstract; cannot be instantiated

32. 接口的方法不能有方法体
    4  MyInterface.java:2: interface methods cannot have body

33. 它是属于抽象类的，不能产生实体
    Myabstract is abstract; cannot be instantiated

34. 接口的方法不能有方法体
    interface methods cannot have body

35. 此处不允许使用static修饰
    asa.java:3: modifier static not allowed here
     public static void main(String []args){
                               ^  ^
                               
36. 不能改变的类型（String 型 不能转换成Int型）
    asa.java:4: inconvertible types
    found   : java.lang.String
    required: int
      int b=(int)a;
                               ^
    1 error
    
37. possible loss of precision  found: long ;required:byte ; var=varlong  可能造成精度损失（在整型较大的转换成较小的情况下会造成损失，小的转大的，则不会造成损失。）

38. 分隔符异常
    asa.java:5: ';' expected
39. 括号异常
    asa.java:8: '}' expected
40. 应用程序试图创建大小为负的数组。
    java.lang.NegativeArraySizeException
41. 出现异常的运算条件
    java.lang.ArithmeticException: / by zero
            at Test2.test(Test2.java:16)
            at Test2.main(Test2.java:5)
42. 抽象方法不能被final修饰（抽象类的抽象的东西一定要被继承）
 
43. 抽象方法不能被private修饰（抽象类抽象的东西一定要被继承）
 
44. Integer number too large  定义值（整数）过大

45. 本次更新
