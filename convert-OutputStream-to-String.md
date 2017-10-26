# Convert OutputStream to String

## How to do it?
If you need to convert OutputStream to String,
you can use the ByteArrayOutputStream class:

```java
ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
writeSomethingToStream(outputStream);
String resultString = outputStream.toString();
```

## Why do we need it?
For example you have a method that writes something to OutputStream and you need its result as a String in Java:

```java
writeSomethingToStream(OutputStream out)
```
