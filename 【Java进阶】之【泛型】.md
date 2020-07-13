# 【Java进阶】之【泛型】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package generics;

import java.util.ArrayList;

class Animal{
	
}

public class App {

	public static void main(String[] args) {
		
//		最初的写法Java5之前
		ArrayList list = new ArrayList();
		list.add("苹果");
		list.add("香蕉");
		list.add("梨子");
		
		String fruit =(String)list.get(1);
		System.out.println(fruit);
		
//		现代的写法
		ArrayList<String> strings = new ArrayList<String>();
		
		strings.add("哈士奇");
		strings.add("泰迪");
		strings.add("中华田园犬");
		
		String animal = strings.get(0);
		System.out.println(animal);
		
		
//		还可以一次性写很多
		HashMap<Integer, String>map = new HashMap<Integer, String>();
		
		ArrayList<Animal> someList = new ArrayList<>();
		
	}

}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



