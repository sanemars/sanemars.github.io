# Android 面试
# [新浪网](http://www.sina.com.cn/)
## IS 部门 Android 笔试题
### Java 基础
1. 打印 result.

```java
int a = 2;
int result = a+++4<<2;
```
`24`

2. 打印 result.

```java
Integer a = 56789;
Integer b = 56789;
boolean result = a==b;
```
`false`

3. 打印 result.

```java
String fun(String s){
    return s.length()>0?(fun(s.substring(1)+s.charAt(0))):"";
}

String result = fun("SinaMail");
```
 `java.lang.StackOverflowError`

4. 写出两种单例模式.(双锁,枚举)
5. 多叉树有哪几种遍历方式?用非递归写出其中一种[遍历算法](https://www.jianshu.com/p/92d25e5c2cd7).(递归遍历、非递归广度优先遍历、非递归深度优先遍历)

### Android基础
1. Activity 和 BroadcastReceiver 的生命周期.
2. 写出 Activity launchMode 并解释.
3. 写出几种 Service 和 Activity 的交互方式.
4. [如何控制多个 Fragment 的显示和隐藏](https://blog.csdn.net/Yu_yan_ran/article/details/73649720),其生命周期有何区别?
5. [UI 线程和非 UI 线程的交互方式](https://blog.csdn.net/zh175578809/article/details/73064810),写出几种各自的耗时.
6. 写出开发中遇到的滑动冲突及解决方式.
7. 如何处理 ScrollView 嵌套 ListView 显示不全的问题?
8. 简述 View 的绘制流程. 测量、布局、绘制
9. 如何规避内存泄漏和溢出,如何排查泄漏或溢出的原因?,
10. 简述对安卓项目架构的理解.

# [新橙科技 iCourt ](http://www.icourt.cc/)

## 双面试官车轮技术面试

TCP 建立链接三次握手和断开链接四次握手

# [摩比神奇](http://www.mobimagic.com/) 实际公司 [闲徕互娱](https://www.lagou.com/gongsi/124192.html)

1. [HashMap 与 HashTable 的区别](https://www.jianshu.com/p/5c34133ed372)
2. 自定义 View 实现特定形状
3. 动画按照指定路径移动

# [酷划在线](http://www.coohua.com/)

1. 设备弱网优化
2. [GC](https://www.cnblogs.com/qlky/p/7325139.html)

# [猎豹移动](http://www.cmcm.com/)

1. 请列举 Android 中常用布局 (Layout) 类型,并简述其用法,以及排版效率.
2. 区别 Animation 和 Animator 的用法,概述实现原理.
3. Thread,Looper,MessageQueue,Handler,Message,每个类的功能是什么,这些类之间是什么关系?
4. 如何加载 NDK 库?如何在JNI中注册 native 函数,有几种注册方法?
5. 操作系统中进程和线程有什么联系和区别? 系统在什么情况下会在用户状态内核态中切换?
6. 如果一个 APP 里面有多进程存在,请列举你所知道的全部IPC方法.
7. 请画出 MPC、MVP 模式的差异.
8. 对于 APP 闪退,可能的原因有哪些?请针对每种情况简述分析过程.
9. 复杂动画优化.

# [Keep](https://gotokeep.com/)

## Unix路径简化

### 题目描述

简化Unix风格的路径，需要考虑的包括"/../","//","/./"等情况

### 输入描述

Unix风格的路径

### 输出描述

简化后的Unix风格路径

### 示例输入

/a/./b/../../c/

### 示例输出

/c

```java

    public void unixBriefPath() {
        String path = "/a/./b/../../c/";
        //path = "/../../c/";
        StringBuilder result = new StringBuilder();
        while (path.startsWith("/..")) {
            path = path.substring(path.indexOf("/..") + 3);
            result.append("/..");
        }
        if (result.length() > 0) {
            result.append("/");
        }
        String prefix = result.toString();
        if (result.length() > 0) {
            result.delete(0, result.length());
        }
        Stack<String> part = new Stack<>();
        String[] paths = path.split("/");
        String temp;
        for (String pt : paths) {
            temp = pt.trim();
            if (temp.length() > 0) {
                if ("..".equals(temp)) {
                    if (!part.isEmpty()) {
                        part.pop();
                    } else {
                        part.push(temp);
                    }
                } else if (!".".equals(temp)) {
                    part.push(temp);
                }
            }
        }
        while (!part.isEmpty()) {
            result.append(part.pop()).append("/");
        }
        if(prefix.length()>0){
            result.deleteCharAt(result.lastIndexOf("/"));
            result.append(prefix);
        }
        result.reverse();
        System.out.println(result.toString());
    }

```

## LRU 原理

# [马蜂窝](http://www.mafengwo.cn/)

1. 自定义 View
2. 多线程
3. View 的工作流程 measure layout draw
4. 动画

# [好未来](http://www.100tal.com/) 2019-12-23
1. Handler 机制
2. [ListView与RecyclerView的区别](https://blog.csdn.net/msc694955868/article/details/80953139)
2. String 转 int 源码
3. [反转链表](https://leetcode-cn.com/problems/reverse-linked-list/solution/fan-zhuan-lian-biao-by-leetcode/)

# [快手](https://www.kuaishou.com/) 2019-12-24
1. Handler 机制
2. View 的滑动冲突
3. [回文链表](https://leetcode-cn.com/problems/palindrome-linked-list/)

# [字节跳动](https://www.bytedance.com/) 2019-12-30
1. [View 过渡绘制优化](https://www.jianshu.com/p/cc893397dc9f)
2. 设计模式
3. [HTTPS](https://blog.csdn.net/qq_38289815/article/details/80969419)
4. View 的事件分发机制 (Activity -> Window -> 顶层 View ; ViewGroup 默认不拦截事件, ViewGroup 的 onInterceptTouchEvent 方法默认返回 false ; View 没有 onInterceptTouchEvent 方法，一旦有点击事件传递给它，那么它的 onTouchEvent 方法就会被调用)

```java
public boolean dispatchTouchEvent (MotionEvent event) { 
    boolean consume = false;
    if (onInterceptTouchEvent (event){
    	consume = onTouchEvent (event);
    } else {
    	consume = child.dispatchTouchEvent (envent);
    }
    
    return consume;
}
```

5. 线程池

```java
public ThreadPoolExecutor (int corePoolSize, 
                                             int maximumPoolSize,
                                             long keepAliveTime, 
                                             TimeUnit unit, 
                                             BlockingQueue<Runnable> workQueue, 
                                             ThreadFactory threadFactory)
```
6. [synchronized关键字加到static静态方法和非static静态方法区别](https://blog.csdn.net/u010391342/article/details/70258159)
7. 图片加载库，列表视图处理(图片的同步加载、图片的异步加载、图片压缩、内存缓存、磁盘缓存、网络拉取 ; imageView 和图片 url 封装成一个对象)
8. 二叉树遍历

```java
        Queue<TreeNode> resultQueue = outPutNode(root, 2);
		while(!resultQueue.isEmpty()) {
			System.out.println(resultQueue.poll().val);
        }

public Queue<TreeNode> outPutNode(TreeNode root,int k) {
		if(root==null || k <= 0 ) return null;
		Queue<TreeNode> queue = new LinkedList<TreeNode>();
		Get(root,k,queue);
		return queue;

private void Get(TreeNode root, int k, Queue<TreeNode> queue) {
		if(root==null || k <= 0 ) return ;
		if(k==1) {
			queue.add(root);
			return;
		}
		if(root.left!=null)
			Get(root.left, k-1, queue);
		if(root.right!=null)
			Get(root.right, k-1, queue);
}

```

9. [主线程 Looper 说明](https://blog.csdn.net/songzi1228/article/details/88710399)
10. Kotlin  标准函数库

| 函数 | 是否传 receiver 值参给 lambda | 是否有相关作用域 | 返回 |
|-|-|-|-|
| let | 是 | 否 | lambda 结果 |
| apply | 否 | 是 | 接受者对象 |
| run | 否 | 是 | lambda 结果 |
| with | 否 | 是 | lambda 结果 |
| also | 是 | 否 | 接受着对象 |
| takeIf | 是 | 否 | 可空类型接受着对象 |
| takeUnless | 是 | 否 | 可空类型接收者对象 |