# Hello World!
       
Hello World is often the first program you learn when learning a new language. The concept is to demonstrate using the output stream to see data in the console.
Specifically, we're seeing the String value between the double quotes (" ").

@[Fix the following c]({"stubs": ["projects/jbc/src/main/java/helloWorld.java"],"command": "javac helloWorld.java"})


    public static void main(String[] args) {

        System.out.println("Hello World!");

    }

# Methods

This early program also demonstrates an example of a method. Specifically, this is the Main method that is usually included in smaller projects. You can also 
have a Main class file instead of having Main methods in every class file. 

Methods are sections of code that can be called or invoked. It's good practice to separate out specific tasks into their own methods. There are also several
built-in methods that come included with Java. When in doubt, try using searching "Java" and specific keywords online. Often, you'll find that someone already 
built a tool you can use in your own code. 

# Keywords / Reserved Words

There are certain keywords in Java that are reserved to serve a specific purpose. In the example above, the words public, static, void, String[], system, 
out, and println are all reserved to mean specific things. "args" is commonly used, but is really only a variable name that can be changed. 

Public refers to the the availability of the file. Think of permissions to view based on being either "public", "protected", and "private". We won't worry too
 much about this in the beginning, but it's something to be aware of.  

Static is related to memory management and needing to create objects or not. Don't worry about this either for now, just know that it needs to be included
when defining methods. 

Void refers to what type of data is returned from this method. You will need to make sure that you use the correct label for your method. If you don't need
to have anything returned, use the "void" keyword. Otherwise, this could be "int", "float", "double", or any primitive variable types. This can also be objects
like "String", "ArrayList", or any object. 



