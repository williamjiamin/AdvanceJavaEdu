# 【Java进阶】之【Set】



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package set;

import java.util.HashSet;
import java.util.LinkedHashSet;
import java.util.Set;
import java.util.TreeSet;

public class App {

	public static void main(String[] args) {
//		没有顺序
//		Set<String> set1 = new HashSet<String>();
//		有顺序
//		Set<String> set1 = new LinkedHashSet<String>();
//		按照自然顺序
		Set<String> set1 = new TreeSet<String>();
		
		if(set1.isEmpty()) {
			System.out.println("这个set是空的");
		}
		
		set1.add("William");
		set1.add("William");
		set1.add("William");
		set1.add("Mary");
		set1.add("Mary");
		set1.add("Mary");
		set1.add("Mary");
		set1.add("Miller");
		set1.add("Miller");
		
		set1.add("William");
		
		System.out.println(set1);
		
		if(set1.isEmpty()) {
			System.out.println("这个set是空的");
		}
		
//		打印每一个元素
		for(String element: set1) {
			System.out.println(element);
		}
		
		if(set1.contains("Tom")) {
			System.out.println("Tom在这个set里面");
		}
		
		if(set1.contains("William")) {
			System.out.println("William在这个set里面");
		}

	}

}

```



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com

 



