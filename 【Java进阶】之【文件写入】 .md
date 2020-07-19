# 【Java进阶】之【文件写入】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package tryWithResources;


class Temp implements AutoCloseable{

	@Override
	public void close() throws Exception {
		System.out.println("The file is closing");
		throw new Exception("Oh somthing is wrong here!!!!");
	}
	
}


public class App {

	public static void main(String[] args) {
		
		try(Temp temp = new Temp()){
			
		} catch (Exception e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}


	}

}

```

App2.java

```java
package tryWithResources;

import java.io.BufferedReader;
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.IOException;

public class App2 {

	public static void main(String[] args) {
		File file = new File("Example.txt11111");
		try(BufferedReader br = new BufferedReader(new FileReader(file))){
			String line;
			while((line =br.readLine()) != null ) {
				System.out.println(line);
			}	
		} catch (FileNotFoundException e) {
			System.out.println("无法找到文件：" +file.toString());
		}catch(IOException e) {
			System.out.println("无法读取文件：" +file.toString());
		}

	}

}

```

App3.java

```java
package tryWithResources;

import java.io.BufferedWriter;
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class App3 {

	public static void main(String[] args) {
		File file = new File("Example2.txt");
		
		try (BufferedWriter bw = new BufferedWriter(new FileWriter(file))){
				bw.write("这个是第一行");
				bw.newLine();
				bw.write("这个是lexueoude.com的课程");
				bw.newLine();
				bw.write("这个是最后一行");
			} catch(IOException e) {
				System.out.println("无法读取文件"+ file.toString());
			}

	}

}

```





乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



