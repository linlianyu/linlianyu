# java经典题目

1.

```
public class ReturnType
{
    public Returntype test(byte x,double y) //第三行
    {
        return (short)x/y;
    }
}

题目：第三行的Returntype应该是什么类型程序才不会报错
```

答案：double

解析：(short)x将byte类型强制换为short类型，再与double进行除运算以后，将会提升为double类型

2.

```
class dad
{
    public float test()
    {
        return 3.0f;
    }
}
class sum extends dad
{
    //第10行
}
题目：一下代码哪个放置在第10行会报错
A:public float test()
  {
      return 4.0f；
  }
B:public void test()
  {

  }
C:public void test(double d)
  {

  }
D:public double test(float x)
  {
      return (double)d;
  }
```

答案：B

解析：A属于方法的重写；B既不属于方法的重写，也不属于方法的重载；C和D属于方法的重载

3.

```
1）public class Test
2）{
3）    public static void main(String args[])
4）    {
5）        int x=3;
6）        int y=1;
7）        if(x=y)
8）        {
9）            System.out.println("x和y相等");
10）       }
11）       else
12）       {
13）           System.out.println("x和y不相等");
14）       }
15）    }
16）}
题目：此段代码哪一行出错了，错在哪？
```

答案：第7行错了，=是赋值运算符，==才是比较运算符

4.

```
public class Foo {
    public static void main(String[] args) {
        try {
            return;
        } finally {
            System.out.println("Finally");
        }
    }
}
题目：程序运行后会有什么结果
A：什么都没有
B：打印"Finally"
C：报错
```

答案：B

解析：在java中，final里面的代码一定会执行，无论程序是否抛出异常

5.

```
public class Test {
    public static String output = "";
    public static void foo(int i) {
        try {
            if (i == 1) {
                throw new Exception();
            }
            output += "1";
        } catch (Exception e) {
            output += "2";
            return;
        } finally {
            output += "3";
        }
        output += "4";
    }
    public static void main(String[] args) {
        foo(0);
        foo(1);
    }
}
题目：程序运行完以后output的值是多少
```

答案：13423

解析：一开始调用foo(0)的时候，output的值为134，调用foo(1)的时候，由于i == 1,所以出现异常，output此时为1342，然后有个return语句，所以output += "4"不会运行，但是finally语句块会运行，所以最后output的值为13423

6.

题目：面向对象的特征主要有哪些方面？

答案：
- 抽象：抽象是将一类对象的共同特征总结出来构造类的过程，包括数据抽象和行为抽象两方面。抽象只关注对象有哪些属性和行为，并不关注这些行为的细节是什么。

- 继承：继承是从已有类得到继承信息创建新类的过程。提供继承信息的类被称为父类(超类、基类);得到继承信息的类被称为子类(派生类)。继承让变化中的软件系统有了一定的延续性，同时继承也是封装程序中可变因素的重要手段(如果不能理解请阅读阎宏博士的《Java与模式》或《设计模式精解》中关于桥梁模式的部分)。

- 封装：通常认为封装是把数据和操作数据的方法绑定起来，对数据的访问只能通过已定义的接口。面向对象的本质就是将现实世界描绘成一系列完全自治、封闭的对象。我们在类中编写的方法就是对实现细节的一种封装;我们编写一个类就是对数据和数据操作的封装。可以说，封装就是隐藏一切可隐藏的东西，只向外界提供最简单的编程接口(可以想想普通洗衣机和全自动洗衣机的差别，明显全自动洗衣机封装更好因此操作起来更简单;我们现在使用的智能手机也是封装得足够好的，因为几个按键就搞定了所有的事情)。

- 多态性：多态性是指允许不同子类型的对象对同一消息作出不同的响应。简单的说就是用同样的对象引用调用同样的方法但是做了不同的事情。多态性分为编译时的多态性和运行时的多态性。如果将对象的方法视为对象向外界提供的服务，那么运行时的多态性可以解释为：当A系统访问B系统提供的服务时，B系统有多种提供服务的方式，但一切对A系统来说都是透明的(就像电动剃须刀是A系统，它的供电系统是B系统，B系统可以使用电池供电或者用交流电，甚至还有可能是太阳能，A系统只会通过B类对象调用供电的方法，但并不知道供电系统的底层实现是什么，究竟通过何种方式获得了动力)。方法重载(overload)实现的是编译时的多态性(也称为前绑定)，而方法重写(override)实现的是运行时的多态性(也称为后绑定)。运行时的多态是面向对象最精髓的东西，要实现多态需要做两件事：1). 方法重写(子类继承父类并重写父类中已有的或抽象的方法);2). 对象造型(用父类型引用引用子类型对象，这样同样的引用调用同样的方法就会根据子类对象的不同而表现出不同的行为)。

7.

题目：访问修饰符public,private,protected,以及不写(默认)时的区别？

答案：

![](https://ws1.sinaimg.cn/large/006tKfTcgy1fr9n3sbenlj30840390sv.jpg)
