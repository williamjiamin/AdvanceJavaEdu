# 【Java进阶】之【getter与setter】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package getter;
class Person{
	String name;
	int age;
	
	void speak() {
		System.out.println("大家好，我是一个机器人，我的名字叫做："+ name );
	}
	
	int calculateHowManyYearsLeft() {
		int yearsLeft = 65 - age;
		return yearsLeft;
	}
	
	int getAge() {
		return age;
	}
	
	String getName() {
		return name;
	}
	
}

public class App {
	public static void main(String[] args) {
		Person person1 = new Person();
		
		person1.name = "William";
		person1.age = 18;
		
		person1.speak();
		
		int years = person1.calculateHowManyYearsLeft();
		
		System.out.println("我离退休还需要工作："+years +"年，OMG！");
		
		int age = person1.getAge();
		String name = person1.getName();
		
		System.out.println("这个人的名字叫做："+name);
		System.out.println("这个人的年龄为："+age);
	
	}
}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



