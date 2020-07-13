# 【Java进阶】之【类型转换】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package casting;

public class App {

	public static void main(String[] args) {
		byte byteValue = 10;
		short shortValue = 20;
		int intValue = 888;
		long longValue = 777;
		
		float floatValue = 8888.8f;
		double doubleValue = 8888.8888;
		
		System.out.println(Byte.MAX_VALUE);

//		做type casting的时候注意这种操作是有风险的
//		byteValue = (byte)128;
//		System.out.println(byteValue);

		intValue = (int)longValue;
		System.out.println(intValue);
		
		
		doubleValue = intValue;
		System.out.println(doubleValue);
		
		intValue = (int)floatValue;
		System.out.println(intValue);
		
		
		
		
	}

}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



