# 【Java进阶】之【多态Polymorphism】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package polymorphism;

public class App {

	public static void main(String[] args) {
		Plant plant1 = new Plant();
		Tree tree = new Tree();

//		Plant plant2 = plant1;
		Plant plant2 = tree;

		plant2.grow();

		tree.stopgrowing();
//	
		ourGrowingFunction(tree);

	}

//		即使没有new一个plant出来，也是可以找到grow，因为与new出来的对象无关，而是与前面的声明有关
//		Plant plant3;
//		plant3.grow();

	public static void ourGrowingFunction(Plant plant) {
		plant.grow();

	}

}

```

Plant.java

```Java
package polymorphism;

public class Plant {
	public void grow() {
		System.out.println("植物正在生长~~~~");
	}
}

```



Tree.java

```java
package polymorphism;

public class Tree extends Plant {

	@Override
	public void grow() {
		System.out.println("树木正在增长~~~");
	}
	
	public void stopgrowing() {
		System.out.println("树木不长了~~~");
	}
}

```





乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



