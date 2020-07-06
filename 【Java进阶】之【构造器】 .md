# 【Java进阶】之【构造器】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



构造器App

```java
package advanced;


class Machine {
	private String UserName;
	private int ID;
	public Machine() {
		this("Tom",6);
		System.out.println("This is the  first Constructor, Be Aware!");
		
		UserName = "William";
	}
	
	public Machine(String UserName) {
		System.out.println("This is a second Constructor! Watch Out!");
		this.UserName = UserName;
	}
	
	public Machine(String UserName, int ID) {
		System.out.println("This is a third Constructor! I am soooo Coool!");
		this.UserName = UserName;
	}
}



public class ConstructorApp {

	public static void main(String[] args) {
		Machine machine1 = new Machine();
//		Machine machine2 = new Machine("William The Secend");
//		Machine machine3 = new Machine("William The Third",3);

	}

}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



