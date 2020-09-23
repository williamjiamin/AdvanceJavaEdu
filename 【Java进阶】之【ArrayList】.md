# 【Java进阶】之【ArrayList】



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package arrayList;

import java.util.ArrayList;

public class App {

	public static void main(String[] args) {
		ArrayList<Integer> numbers = new ArrayList<Integer>();
		
//		Add something to the ArrayList
		numbers.add(99);
		numbers.add(88);
		numbers.add(100);
		
//		Output somthing out of the ArrayList
//		System.out.println(numbers.get(2));
		
//		for(int i=0; i < numbers.size(); i ++) {
//			System.out.println(numbers.get(i));
//		}
		
		for(Integer value: numbers) {
			System.out.println(value);
		}
	}

}

```



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com

 



