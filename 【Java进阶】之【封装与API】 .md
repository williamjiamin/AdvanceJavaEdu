# 【Java进阶】之【封装与API】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package encapsulation;


class Plant{
	public static final int ID = 888;
	private String name;
	
	public String getData() {
		String data = "Something" + calculateStockMarket();
		return data;
	}
	
	
	private int calculateStockMarket() {
		return 10;
	}

	public String getName() {
		return name;
	}

	public void setName(String name) {
		this.name = name;
	}
	
}


public class App {

	public static void main(String[] args) {
		

	}

}

```



API文档：https://tool.oschina.net/apidocs/apidoc?api=jdk-zh

英文：https://docs.oracle.com/javase/8/docs/api/java/lang/String.html



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



