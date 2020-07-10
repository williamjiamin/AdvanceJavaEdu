# 【Java进阶】之【toString】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package toStringIntro;

class Person{
	private int id;
	private String name;
	
	public Person(int id, String name) {
		this.id =id;
		this.name = name;
	}
	
	public String toString() {

//		通过String Cat的方式，效率不高
//		return "Hello , I am William";
//		return id + ": " + name;
		
//		通过StringBuilder的方式，日常开发使用较多
//		StringBuilder sb = new StringBuilder();
//		sb.append(id).append(":  ").append(name);
		
//		return sb.toString();
		return String.format("%-4d: %s", id, name);
	
	
	}
	
}


public class App {

	public static void main(String[] args) {
		Person person1 = new Person(8,"William");
		Person person2 = new Person(9,"Tommy");
		System.out.println(person1);
		System.out.println(person2);

	}

}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



