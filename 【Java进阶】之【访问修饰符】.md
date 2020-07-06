# 【Java进阶】之【访问修饰符】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package accessmod;

public class App {

	public static void main(String[] args) {
		Plant plant = new Plant();
		System.out.println(plant.name);
		System.out.println(plant.ID);
		System.out.println(plant.type);

	}

}

```

grass.java

```Java
package accessmod;

public class grass extends Plant {

	public tree() {
		type = "tree01";
		
	}
}

```



Plant.java

```java
package accessmod;

public class Plant {
	//	这个做法不好！
	public String name;
	
	//好的做法
	public final static int ID = 888888;
	
	private String type;
	
	public Plant() {
		this.name = "William Inc.";
		this.type = "plant";
	}
}

```





乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



