# 【Java进阶】之【异常处理】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
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

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



