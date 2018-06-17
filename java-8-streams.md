# Java 8 Streams Tutorial

Welcome to the Java 8 tutorial for streams!

First let's define our testing variable for this tutorial:

```java
final List<String> names = Arrays.asList(
    "John Lennon",
    "Paul McCartney",
    "George Harrison",
    "Ringo Starr");
```

Let's say we want to convert every item on this list to upper case
and then filter out only those variables, that contain the letter "E".

## Java 7

In Java 7 or older, we would have to do something like this:

```java
final List<String> result = new ArrayList<>();

for (final String name : names) {
    final String toUpperCase = name.toUpperCase();
    if (toUpperCase.contains("E")) {
        result.add(toUpperCase);
    }
}

return result;
```

What bothers us about the above code:
* we need a new variable to collect data to the result
* we had to use a for loop to iterate over the values
* we define another variable to store the upper case value

## Java 8
In Java 8, we can rewrite the example above like this:
```java
return names.stream()
        .map(String::toUpperCase)
        .filter(s -> s.contains("E"))
        .collect(Collectors.toList());
```

In this tutorial, we used these great Java 8 features:
* streams
* mapping
* filters
* collectors

## Download

This tutorial is available for download!

If you want to run and test all of this in a Java code:

[download or clone git repository with Java 8 tutorials](https://github.com/slady/Java-8-tutorial)