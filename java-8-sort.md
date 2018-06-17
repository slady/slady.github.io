# Java 8 Sort Example

Welcome to the Java 8 tutorial for sorting an array!

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