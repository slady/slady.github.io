# XML marshalling in Java

```java
JAXBContext context = null;
try {
    context = JAXBContext.newInstance(YourDesiredClass.class);
    Marshaller marshaller = context.createMarshaller();
    StringWriter sw = new StringWriter();
    marshaller.marshal(validate, new StreamResult(sw));
    Files.write(Paths.get("/tmp/outputFile.xml"), sw.toString().getBytes());
} catch (JAXBException e) {
    e.printStackTrace();
}
```

...and that's all you need to do for manual XML marshalling in Java!