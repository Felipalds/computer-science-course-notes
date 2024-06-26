> Serialization is the conversion of the state of an object into a byte array (to transfer via network or save in a database/file). Deserialization does the opposite.

- Platform independent: we can serialize an object in one platform and then deserialize in another. Java handles with the complexity of the platform, such as endianness and architecture.
- JVM allows cross-platform compatibility.
- Static atributes are not serializable
- Transient keyword says to Java to not serialize an atribute

## Serialization:
``` 
FileOutputStream fileOut = new FileOutputStream("person.ser");  
ObjectOutputStream out = new ObjectOutputStream(fileOut);  
out.writeObject(person);
```

## Deserialization:
```
FileInputStream fileIn = new FileInputStream("person.ser");  
ObjectInputStream in = new ObjectInputStream(fileIn);  
Person person2 = (Person) in.readObject();
```

We need these classes:
1. FileOutputStream
2. ObjectOutputStream

1. FileInputStream
2. ObjectInputStream

Both ObjectOutputStream and ObjectInputStream are high level classes that extends the InputStream class.


## Inheritance and Composition
1. A Serializable class subclasses are also serializable
2. The composition class must implement Serializable manually
## UID
1. The Serializable classes must have a serialVersionUID
	1. Most of IDEs puts it automatically but it is highly recommended

## Custom functions
```
private void writeObject(ObjectOutputStream oos) throws IOException {
		 oos.defaultWriteObject(); 
		 oos.writeObject(address.getHouseNumber()); 
} 
private void readObject(ObjectInputStream ois) throws ClassNotFoundException, IOException { 
	ois.defaultReadObject(); 
	Integer houseNumber = (Integer) ois.readObject(); 
	Address a = new Address(); 
	a.setHouseNumber(houseNumber); this.setAddress(a); 
}
```