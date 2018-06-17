# Java 8 Sort Example

Welcome to the Java 8 tutorial for sorting an array!

## Java 7
If we were working in Java 7 or any later version of Java before 8, we would do this:

```java
final List<String> names = Arrays.asList("John Lennon", "Paul McCartney", "George Harrison", "Ringo Starr");

Collections.sort(names, new Comparator<String>() {
    @Override
    public int compare(String a, String b) {
        return a.compareTo(b);
    }
});

for (final String name : names) {
    System.out.println(name);
}
```

This is not so bad, but we know we can do it better in Java 8.

## Java 8

We start with removing the unnecessary anonymous inner class definition, that is not needed in Java 8:
```java
Collections.sort(names, (String a, String b) -> {
    return a.compareTo(b);
});
```

Then we can remove the method definition like this:
```java
Collections.sort(names, (String a, String b) -> a.compareTo(b));
```

And Java 8 does not require method parameter types definition:
```java
Collections.sort(names, (a, b) -> a.compareTo(b));
```

Now comes a real great feature of Java 8, that is a method reference:
```java
Collections.sort(names, String::compareTo);
```

That was a huge step forward! But Java 8 offers us even a sort method on the array object itself:
```java
names.sort(String::compareTo);
```

This is great! Can we use this principle for printing?

Sure, we use for each loop on the array object,
together with a method reference, that we already know:
```java
names.forEach(System.out::println);
```

If you want to test all of this in a Java code, download or clone this
[java.ps git repository with Java 8 tutorials](https://github.com/slady/Java-8-tutorial)
