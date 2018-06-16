# Running a single test in maven

During development, you may run a single test class repeatedly.
If you run maven from the command line, these tutorials will come in handy.

There are differences between a single **unit** test and a single **integration** test.
These two cases will be described bellow.

## Running a single unit test in maven
In the case of a **single unit test in maven**, there is this **Maven Surefire Plugin** parameter:

```sh
mvn -Dtest=TestCircle test
```

Notice the 'test' phase and the 'test' parameter name!

You may also use patterns to run a number of tests:

```sh
mvn -Dtest=TestCi*le test
```

Or you may use multiple names/patterns, separated by commas:
  mvn -Dtest=TestSquare,TestCi*le test

## Running a single integration test in maven
In the case of a **single integration test in maven**, there is this **Maven Failsafe Plugin** parameter:

```sh
mvn -Dit.test=ITCircle verify
```

Notice the 'verify' phase and the 'it.test' parameter name!

You may also use patterns to run a number of tests:

```sh
mvn -Dit.test=ITCi*le verify
```

And you may use multiple names/patterns, separated by commas:

```sh
mvn -Dit.test=ITSquare,ITCi*le verify
```

## Running a set of methods in a single test class
You can run only a subset of the test methods in a test class.

The separator character between a class name and a method name is the **hash mark** character '#', for example:
```sh
mvn -Dit.test=ITCircle#mytest verify
```

You can use patterns too

```sh
mvn -Dit.test=ITCircle#test* verify
```

As of Surefire 2.12.1, you can select multiple methods (JUnit 4.x only at this time; patches welcome!):

```sh
mvn -Dit.test=ITCircle#testOne+testTwo verify
```
