# Java 8 Files Example

Welcome to the Java 8 files tutorial!

First let's define our testing variable for this tutorial:

## Read file line by line

Let's say we want to read a whole file line after line
and print each line to the output console.

### Java 7

In Java 7, we would have to iterate like this:

```java
try (final BufferedReader br = new BufferedReader(new FileReader(fileName))) {
    String line;
    while ((line = br.readLine()) != null) {
        System.out.println(line);
    }
}
```

This boiler plate code is very cumbersome. Let's see what Java 8 has to offer.

### Java 8
In Java 8, we can simply write this:
```java
Files.readAllLines(Paths.get(fileName)).forEach(System.out::println);
```

That's all folks! ;)

## Download

This tutorial is available for download!

If you want to run and test all of this in a Java code:

[download or clone git repository with Java 8 tutorials](https://github.com/slady/Java-8-tutorial)