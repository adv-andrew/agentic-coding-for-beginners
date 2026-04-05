# Java OOP Project

Java project using object-oriented programming principles.

## Rules
- Java 17
- No external libraries (standard library only)
- camelCase methods, PascalCase classes
- Every public method needs a Javadoc comment
- No wildcard imports (use specific imports)

## Project Structure
- src/ -- all source files
- tests/ -- JUnit test files

## How to Compile and Run
- javac src/*.java
- java -cp src Main

## How to Run Tests
- javac -cp .:junit-5.jar tests/*.java
- java -cp .:junit-5.jar org.junit.runner.JUnitCore TestSuite

## Constraints
- Must implement Comparable interface
- Must override toString(), equals(), and hashCode()
- No use of ArrayList (must use arrays)
