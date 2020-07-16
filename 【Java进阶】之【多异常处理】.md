# 【Java进阶】之【多异常处理】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package multipleException;

import java.io.FileNotFoundException;
import java.io.IOException;
import java.text.ParseException;

public class App {

//	public static void main(String[] args) throws IOException, ParseException {
//		Test  test = new Test();
//		test.run();

//	public static void main(String[] args) {
//		Test test = new Test();
//		try {
//			test.run();
//		} catch (IOException e) {
//			// TODO Auto-generated catch block
//			e.printStackTrace();
//		} catch (ParseException e) {
//			// TODO Auto-generated catch block
//			e.printStackTrace();
//		}

	public static void main(String[] args) {
		Test test = new Test();

//		try {
//			test.run();
//		} catch (Exception e) {
//			e.printStackTrace();
//		}
		package exceptionHandling;

		import java.io.File;
		import java.io.FileNotFoundException;
		import java.io.FileReader;
		public class App {

			public static void main(String[] args) {
				File file = new File("Example.txtaaaaa");
				
				try {
					FileReader fr = new FileReader(file);
				} catch (FileNotFoundException e) {
					System.out.println("文件未找到错误，未找到名字为："+ file.toString() +"的文件！");
				}
				

			}

		}

//		try {
//			test.run();
//		} catch (IOException | ParseException e) {
//			e.printStackTrace();
//		}
		
		try {
			test.input();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}catch(FileNotFoundException  e) {
			e.printStackTrace();
		}
		

	}

}

```

Test.java

```java
package multipleException;

import java.io.FileNotFoundException;
import java.io.IOException;
import java.text.ParseException;

public class Test {
	public void run() throws IOException, ParseException {
//		throw new IOException();
		
		throw new ParseException("Error in parsing at",3);
	}
	
	public void input() throws IOException, FileNotFoundException{
		
	}
}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



