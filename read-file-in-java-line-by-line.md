# reading file in java line by line

To read file in Java line by line, use the readLine() method from the `BufferedReader` class.

Example source code:

```java
BufferedReader br = new BufferedReader(new FileReader(file));
String line;
while ((line = br.readLine()) != null) {
   // process the line.
}
br.close();
```