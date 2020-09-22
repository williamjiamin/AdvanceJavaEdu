# 【Java进阶】之【Serialization】



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com



Person.java

```java
package serialization;

import java.io.Serializable;

public class Person  implements Serializable {
	private int id;
	private String name;
	
	public Person(int id, String name) {
		this.id = id;
		this.name = name;
	}

	@Override
	public String toString() {
		return "Person [id=" + id + ", name=" + name + "]";
	}
	
	
	
	
	
}

```

ReadObjects.java

```java
package serialization;

import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.ObjectInputStream;
import java.util.ArrayList;

public class ReadObjects {
	public static void main(String[] args) throws ClassNotFoundException {
		System.out.println("正在读取Objects......");
		
		try(FileInputStream fi = new FileInputStream("person.bin")){
			
			ObjectInputStream os = new ObjectInputStream(fi);
			
//			Person person1 = (Person)os.readObject();
//			Person person2 = (Person)os.readObject();
//			
			Person[] people = (Person[])os.readObject();
			
			ArrayList<Person> peopleList = (ArrayList<Person>)os.readObject();
			
			for(Person person: people) {
				System.out.println(person);
			}
			
			
			
			for(Person person: peopleList) {
				System.out.println(person);
				
			}
		
			int num = os.readInt();
			
			for(int i=0; i<num; i++) {
				Person person = (Person)os.readObject();
				System.out.println(person);
			}
			
			os.close();
			
//			System.out.println(person1);
//			System.out.println(person2);
			
		} catch (FileNotFoundException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		
	}
	
}

```

WriteObjects.java

```java
package serialization;

import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.ObjectOutputStream;
import java.util.ArrayList;
import java.util.Arrays;

public class WriteObjects {

	public static void main(String[] args) {
		System.out.println("我们正在写入Object......");
		
//		Person william = new Person(111, "William");
//		Person mary = new Person(222, "Mary");
		
		Person[] people = {new Person(1,"William"), new Person(2,"Tom"), new Person(3,"Mike")} ;
		
		ArrayList<Person> peopleList =new ArrayList<Person>(Arrays.asList(people));
		
//		System.out.println(william);
//		System.out.println(mary);
		
		try(FileOutputStream fs = new FileOutputStream("person.bin")){
			ObjectOutputStream os = new ObjectOutputStream(fs);
			
//			os.writeObject(william);
//			os.writeObject(mary);
			
			os.writeObject(people);
			
			os.writeObject(peopleList);
			
			
			os.writeInt(peopleList.size());
			
			for(Person person: peopleList) {
				os.writeObject(person);
			}
			
			
			os.close();
			
		} catch (FileNotFoundException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}

		
		
	}

}

```



乐学偶得版权所有  公众号1： 乐学偶得  公众号2：乐学Fintech  正版视频课程 lexueoude.com

 



