# 【Java进阶】之【类与继承】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package advanced2;

public class App {
	public static void main(String[] args ) {
//		Machine mach1 = new Machine();
//
//		mach1.transform();
//		mach1.talk();
		
		Car car1 = new Car();
		
		
		car1.talk();
		car1.transform();
		car1.runningsooofast();
		
	}
}

```

Car.java

```Java
package advanced2;

public class Car extends Machine {
	
	@Override
	public void transform() {
		System.out.println("我是变形金刚，我从车变成变形金刚啦~");
	}

	public void runningsooofast() {
		System.out.println("我是一个神跑车，我跑到炒鸡快！");
	}
}

```



Machine.java

```java
package advanced2;

public class Machine {
	public void transform() {
		System.out.println("我开始变形了！");
	}
	public void talk() {
		System.out.println("我这个机器人正在说话");
	}
	
}

```





乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



