# 【Java进阶】之【内部类】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package innerClass;

public class App {

	public static void main(String[] args) {
		Robot robot = new Robot(888);
		robot.start();

//		Robot.Brain brain = robot.new Brain();
//		
//		brain.think();
		
//		Robot.Battery battery = new Robot.Battery();
//		battery.charge();
		
	}

}

```

Robot.java

```java
package innerClass;

public class Robot {
	private int id;

	
//	可以将private改成public，这样在App内调用
	private class Brain{
		public void think() {
			System.out.println("机器人"+id+"已经开始思考了！！！");
		}
	}
	
	
	public static class Battery{
		public void charge() {
			System.out.println("机器人正在充电ing~");
		}
	}
	
	public Robot(int id) {
		this.id = id;
	}
	
	public void start() {
		System.out.println("机器人已经启动，编号为：" +id);
		
		Brain brain =new Brain();
		brain.think();
		
		final String name ="lexueoude.com";
		
		class Temp {
			public void doSomething() {
				System.out.println("大家好，我这个机器人的ID号为：" + id );
				System.out.println("我的名字为：" + name);
			}
		}
		
		Temp temp = new Temp();
		temp.doSomething();
		
	}
	
}

```





乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



