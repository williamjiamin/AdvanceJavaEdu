# 【Java进阶】之【文件读取】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package readingFile;

import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;


public class App {

	public static void main(String[] args) throws FileNotFoundException {
//		其中一种写法（绝对路径）
//		String fileName = "C:\\Users\\yons\\Desktop\\Example.txt";
//		String fileName = "C:/Users/yons/Desktop/Example.txt";
	
//		另一种相对路径
		String fileName = "Example.txt";

		File textFile = new File(fileName);
		
		Scanner in = new Scanner(textFile);
		
		int value = in.nextInt();
		System.out.println("1:I have read the number,which is {" +value +"}" );
		
		in.nextLine();
		
		int count = 2;
		while(in.hasNextLine()) {
			String line = in.nextLine();
			
			System.out.println(count +":"+ line);
			count++;
		}
		
		in.close();
		
	}

}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



