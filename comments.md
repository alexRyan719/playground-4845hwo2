# Comments

Comments are text that is ignored by compilers and are very useful in programming. You can use comments to explain your code to others, debug, and even layout
a blue print for building your code (psuedocode).

    // This is a single line comment.

    /*
    This 
    is 
    a 
    multi line
    comment
    */

Comments can be used to describe sections of your code. 

    // This is the main method. It prints the string "Hello World" to the console. 
    public static void main(String[] args) {

        System.out.println("Hello World!");

    }

Comments are also useful when debugging your code.

    public static int add(int num1, int num2){

        return num1 - num2;

    }


    public static void main(String[] args) {

        // I should be getting 8...but I'm getting 2?
        System.out.println(add(5,3));

    }