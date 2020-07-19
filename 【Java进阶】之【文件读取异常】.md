# 【Java进阶】之【文件读取异常】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package fileReader;

import java.io.BufferedReader;
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.IOException;

public class App {

	public static void main(String[] args) {
		
		File file = new File("Example.txtaaaaaa");
		
		BufferedReader br =null;
		
		try {
			FileReader fr = new FileReader(file);
			br = new BufferedReader(fr);
			
			
			String line;
			
			while((line = br.readLine()) != null );
			System.out.println(line);
		
		} catch (FileNotFoundException e) {
			 System.out.println("文件未找到错误，请查看是否确定有这个文件名的文件：" +file.toString());
		} catch (IOException e) {
			// TODO Auto-generated catch block
			System.out.println("文件无法进行读取，请查看这个文件名的文件是否完整：" +file.toString());
		}
		
		finally {
			try {
				br.close();
			} catch (IOException e) {
				System.out.println("无法关闭文件");
			}
			catch(NullPointerException ex) {
				//文件因为某些原因未打开
			}
		}
		
		
	}

}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



