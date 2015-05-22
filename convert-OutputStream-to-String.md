If need to convert OutputStream to String,
you can use the ByteArrayOutputStream class:
		ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
		writeSomethingToStream(outputStream);
		String resultString = outputStream.toString();

When do we need it?
For example you have a method that writes something to OutputStream and you need its result as a String in Java:
		writeSomethingToStream(OutputStream out)
