Use the System Property called "user.dir".

Example source code:

public class GetTheCurrentWorkingDirectoryInJava {
  public static void main(String[] args) {
       System.out.println("Working Directory = " +
              System.getProperty("user.dir"));
  }
}
