# 【Java进阶】之【HashMap】



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package hashMap;

import java.util.HashMap;
import java.util.Map;

public class App {

	public static void main(String[] args) {
		HashMap<Integer, String> map = new HashMap<Integer, String>();
		
		map.put(1,"One");
		map.put(2,"Two");
		map.put(3,"Three");
		map.put(4,"Four");
		map.put(5,"Five");
		map.put(6,"Six");
		
		String text = map.get(3);
		System.out.println(text);

		for(Map.Entry<Integer, String> entry: map.entrySet()){
			int key = entry.getKey();
			String value = entry.getValue();
			
			System.out.println("id号为："+key + "，值为：" + value);
		}
		
		
	}

}

```



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com

 



