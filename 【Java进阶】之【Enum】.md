# 【Java进阶】之【Enum】



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package enum_intro;

public class App {

//	public static final int CAT = 0;
//	public static final int DOG = 1;
//	public static final int MOUSE = 3;
	
	public static void main(String[] args) {
		
//		int animal = CAT;
		Animal animal = Animal.CAT;
		
		switch(animal) {
		case CAT:
			System.out.println("Hi, 这个是猫");
			break;
		case DOG:
			System.out.println("Hi, 这个是狗");
			break;
		case MOUSE:
			System.out.println("Hi, 这个是老鼠");
			break;
		default:
			break;
//		case DOG:
//			System.out.println("狗");
//			break;
//		case MOUSE:
//			System.out.println("狗");
//			break;	
//		
			
		
		}
//一种具体理解的思路
		System.out.println(Animal.CAT);
		System.out.println(Animal.CAT.getClass());
		System.out.println(Animal.CAT instanceof Enum);

		
	}

}

```

Animal.java

```java
package enum_intro;

public enum Animal {
	DOG, CAT, MOUSE
}

```





乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com

 



