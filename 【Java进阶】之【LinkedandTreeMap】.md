# 【Java进阶】之【LinkedandTreeMap】



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com



App.java

```java
package linkandtreemap;

import java.util.HashMap;
import java.util.LinkedHashMap;
import java.util.Map;
import java.util.TreeMap;

public class App {
	public static void main(String[] args) {
		HashMap<Integer, String> hashMap = new HashMap<Integer, String>();
		LinkedHashMap<Integer, String> linkedhashMap = new LinkedHashMap<Integer, String>();
		TreeMap<Integer, String> treeMap = new TreeMap<Integer, String>();
		
		testMap(treeMap);
	}

	public static void testMap (Map<Integer, String> map) {
		map.put(9,"William");
		map.put(5,"Jim");
		map.put(6,"Mike");
		map.put(2,"Watt");
		map.put(3,"Kate");
		map.put(7,"Will");
		map.put(1,"Mary");
		
		for(Integer key: map.keySet()) {
			String value = map.get(key);
			
			System.out.println(key + ":" + value);
		}
	}
	
}

```



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com

 



