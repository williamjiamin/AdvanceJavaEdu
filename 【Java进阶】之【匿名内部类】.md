# 【Java进阶】之【匿名内部类】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package anonymousClass;

class Machine {
	public void start() {
		System.out.println("Machine Started~");
	}
}

interface Plant {
	public void grow();
}

public class App {
	public static void main(String[] args) {
		Machine machine1 = new Machine() {
			@Override
			public void start() {
				System.out.println("iphone started!!!");
			}

		};
		machine1.start();

		Plant plant1 = new Plant() {

			@Override
			public void grow() {
					System.out.println("The Plant is growing right now~");
			}

		};
		
		plant1.grow();

	}
}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



