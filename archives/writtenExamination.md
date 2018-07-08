# Sina
## Android 笔试题
### Java 基础
1. 打印 result.

```java
int a = 2;
int result = a+++4<<2;
```

2. 打印 result.

```java
Integer a = 56789;
Integer b = 56789;
boolean result = a==b;
```

3. 打印 result.

```java
String fun(String s){
    return s.length()>0?(fun(s.substring(1)+s.charAt(0))):"";
}

String result = fun("SinaMail");
```

4. 写出两种单例模式.
5. 多叉树有哪几种遍历方式?用非递归写出其中一种遍历算法.

### Android基础
1. Activity 和 BroadcastReceiver 的生命周期.
2. 写出 Activity launchMode 并解释.
3. 写出几种 Service 和 Activity 的交互方式.
4. 如何控制多个 Fragment 的显示和隐藏,其生命周期有何区别?
5. UI 线程和非 UI 线程的交互方式,写出几种各自的耗时.
6. 写出开发中遇到的滑动冲突及解决方式.
7. 如何处理 ScrollView 嵌套 ListView 显示不全的问题?
8. 简述 View 的绘制流程.
9. 如何规避内存泄漏和溢出,如何排查泄漏或溢出的原因?
10. 简述对安卓项目架构的理解.
