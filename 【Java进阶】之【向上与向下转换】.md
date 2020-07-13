# 【Java进阶】之【类型转换】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package upAndDownCasting;

class Machine{
	public void start() {
		System.out.println("机器启动啦！");
	}
}

class Camera extends Machine {
	public void start() {
		System.out.println("照相机启动啦！");
	}
	
	public void snap() {
		System.out.println("照相机照相啦！");
	}
}




public class App {
	public static void main(String[] args) {
			Machine machine1 = new Machine();
			Camera camera1 = new Camera();
			
//			machine1.start();
//			如果方法未定义，则无法执行
//			machine1.snap();
			camera1.start();
//			camera1.snap();

//			upcasting
			Machine machine2 = camera1;
			machine2.start();
//			这样不行，因为machine里面没有snap方法
//			machine2.snap();
			
			
//			downcasting
			Machine machine3 = new Camera();
			machine3.start();
//			在做downcasting的时候，需要提供具体cast的类型在括号中
			Camera camera2 = (Camera)machine3;
			camera2.start();
			camera2.snap();
			
	}

}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



