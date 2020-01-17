# XLSX Reader

This java class makes it easy to read and use data from `.xlsx` files.

## Installation

If you are using **Maven** project then you just need to add some dependencies to your `pom.xml` and throw in `XLSXreader.java` in to your project

```XML
<dependencies>

		<dependency>
			<groupId>org.apache.poi</groupId>
			<artifactId>poi</artifactId>
			<version>4.1.1</version>
		</dependency>

		<dependency>
			<groupId>org.apache.poi</groupId>
			<artifactId>poi-ooxml</artifactId>
			<version>4.1.1</version>
		</dependency>

	</dependencies>
```

## Usage

```java
XLSXreader xlsx = new XLSXreader("example.xlsx");

xlsx.getItem("username", 0);
//returns a first item from "username" column 

xlsx.size();
//returns the number of values that are in one column (not including key values)

xlsx.keySize();
//returns the number of key values

xlsx.containsKey("username");
//returns ture or false. It checks if the "key" exists

xlsx.containsValue("user1");
//returns true or false. It checks if the "value" exists

xlsx.containsValueByKey("user1", "username");
//returns true or false. It checks if the "value" exists in side a column with a specified key
```

## Method list
- getItem(String key, int index) -> returns String
- keySize() -> returns int 
- size() -> returns int
- containsKey(String key) -> returns boolean
- containsValue(String value) -> returns boolean
- containsValueByKey(String value, String key) -> returns boolean
- toString() -> returns String