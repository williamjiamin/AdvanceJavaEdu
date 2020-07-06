# 【Java进阶】之【接口】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package interface_intro;

public class App {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Machine mach1 = new Machine();
		mach1.start();
		
		System.out.println("...................................");
	
		
		Person person1 = new Person("William");
		person1.greet();
		
		System.out.println("...................................");
		
		Info info1 = new Machine();
		info1.showInfo();

		System.out.println("...................................");
		
		Info info2 = person1;
		info2.showInfo();
		
		System.out.println("...................................");
		
		OutPutOurInfo(mach1);
		OutPutOurInfo(person1);
		
		
	}
	private static void OutPutOurInfo (Info info) {
		info.showInfo();
	}

}

```

Info.java

```Java
package interface_intro;

public interface Info {
	public void showInfo();
}

```



Machine.java

```java
package interface_intro;

public class Machine implements Info {
	private int id = 888;
	public void start() {
		System.out.println("我这个机器已经开动咯~");
	}
	
	
	@Override
	public void showInfo() {
		System.out.println("报告，我这个机器的id号码是："+id);
		
	}
}

```

Person.java

```java
package interface_intro;

public class Person implements Info {
	private String name;
	public Person(String name) {
		this.name = name;
	}
	public void greet() {
		System.out.println("Hello,我是一个人");
	}
	

	public void showInfo() {
		System.out.println("这个人的名字叫做："+name);
		
	}
}

```





乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



