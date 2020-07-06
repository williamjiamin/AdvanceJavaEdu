# 【Java进阶】之【多线程】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



计数君App

```java
package advanced;

class Runner extends Thread {
	public void run() {
		for (int i=0; i<50;i++) {
			System.out.println("我正在哼哧哼哧的计算ing，计数君来了：" + i );			
			try {
				Thread.sleep(500);
			} catch (InterruptedException e) {
				// TODO Auto-generated catch block
				e.printStackTrace();
			}				
		}	
	}	
}

public class App {
	public static void main(String[] args) {
		Runner runner1 = new Runner();
		runner1.start();
		
		Runner runner2 = new Runner();
		runner2.start();
		
		Runner runner3 = new Runner();
		runner3.start();
		
		Runner runner4 = new Runner();
		runner4.start();
		
		Runner runner5 = new Runner();
		runner5.start();
	}
}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



