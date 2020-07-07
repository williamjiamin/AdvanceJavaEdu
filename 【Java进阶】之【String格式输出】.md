# 【Java进阶】之【String与格式输出】



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package string;

public class App {
		public static void main(String[] args) {
			
			//这种写法是可以的，但是不推荐，因为效率很低
			String something_to_say = "";
			
			something_to_say +="Hello.";
			something_to_say += "My name is William";
			something_to_say += "Welcome to lexueoude.com";
			
			System.out.println(something_to_say);
			
			
//			通过StringBuilder进行实现，推荐，效率更高
		    StringBuilder sb = new StringBuilder("");
		    sb.append("Hello");
		    sb.append("......");
		    sb.append("Welcome to lexueoude.com");
		    
		    System.out.println(sb.toString());
		    
		    
//		    更加简洁的写法
		    StringBuilder sb2 = new StringBuilder();
		    sb2.append("Hello2")
		    .append("......2")
		    .append("Welcome to lexueoude.com...2");
		    
		    System.out.println(sb2.toString());
			
		
//		    String可以做各种格式变换（按照某种格式进行输出）
		    System.out.print("I am William from lexueoude.com. \t 公众号：乐学FinTech \n  这是下面一行");
		    
//		    Intergers格式输出
		    System.out.printf("I am William . I am %d year old\n",1);
		    
		    for (int i=0; i<50; i++) {
		    	System.out.printf("%2d: %s\n",i,"somthing");
		    }
		    
//		    float的格式输出
		    System.out.printf("数字是： %.2f \n", 1.23456789);
		    System.out.printf("另数字是： %6.3f \n", 1.23456789);
		}
}

```



乐学偶得版权所有  公众号：乐学Fintech  正版视频课程 lexueoude.com

 



