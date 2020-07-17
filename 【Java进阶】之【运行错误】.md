# 【Java进阶】之【运行错误】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package runtimeException;

public class App {

	public static void main(String[] args) {

//checked exception，必须在写代码的时候就需要处理的
//		try {
//			Thread.sleep(100);
//		} catch (InterruptedException e) {
//			// TODO Auto-generated catch block
//			e.printStackTrace();
//		}
		
//		uncheck exception(runtime exception)
//		int value = 888;
//		value = value/0;
		
//		String text = null;
//		System.out.println(text.length());

		String[] texts = {"one","two","three","four","five"};
		
//		try {
//		System.out.println(texts[5]);
//		}catch(RuntimeException e) {
//			System.out.println(e.toString());
//			
//		}
		try {
		System.out.println(texts[5]);
		}catch(ArrayIndexOutOfBoundsException e) {
			System.out.println(e.toString());
			
		}		
		
		
	}

}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



