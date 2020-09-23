# 【Java进阶】之【LinkedList】



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package linkedList;

import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;

public class App {
	public static void main(String[] args) {
		List<Integer> arrayList = new ArrayList<Integer>();
		List<Integer> linkedList = new LinkedList<Integer>();
		
		doTimings("ArrayList", arrayList);
		doTimings("LinkedList", linkedList);
	}
	
	private static void doTimings(String type, List<Integer> list) {
			
			for(int i=0; i <1E5; i++) {
				list.add(i);
			}
			
			long start = System.currentTimeMillis();
			
//			在末尾添加
//			for(int i=0; i<1E5; i++) {
//				list.add(i);
//			}
			for(int i =0; i <1E5; i++) {
				list.add(0,1);
			}

			long end = System.currentTimeMillis();
			
			System.out.println("花费的时间为" +(end - start )+ "ms, 使用的类型为：" + type);
			
		
	}

}

```



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com

 



