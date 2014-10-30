To read file inJ ava line by line, use the readLine() method from the BufferedReader class.

Example source code:

BufferedReader br = new BufferedReader(new FileReader(file));
String line;
while ((line = br.readLine()) != null) {
   // process the line.
}
br.close();
