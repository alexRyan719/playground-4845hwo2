# Loops

Loops are useful when you want to do the same thing, just many times. If you already know exactly how many times you want the loop to run / iterate, you 
should use a for loop. If you want the loop to be scalable for varying sizes / iterations, use a while loops. If you want a process to happen once and 
THEN a loop, use a do while loop. However, do while loops might not exist in other languages. There are ways to simulate a do while loop, as well as 
simulate any type of loop (and even recursion) with the other types.  

    public static void forLoop(int size) {
		
		for(int i = 0; i < size; i++) {
			System.out.println(i);
		}
		
	}
	
	public static int whileLoop(int size) {
		
		if(size <= 0) {
			System.out.println(size);
			return 0;
		}
		
		while(size > 0) {
			System.out.println(size);
			size--;
		}
		
		return 0;
		
	}
	
	public static int doWhileLoop(int size) {
		
		// Error handling for input less than zero -> infinite loop
		if(size <= 0) {
			System.out.println(size);
			return 0;
		}
		
		do {
			System.out.println(size);
			size--;
		} while(size > 0);
		
		return 0;
		
	}
	
	public static int recursion(int size) {
		
		System.out.println(size);
		if(size == 0) {
			return 0;
		} else {
			return recursion(size - 1);
		}

	}
	
	public static void main(String[] args) {
		
		System.out.println("For Loop of 5: ");
		forLoop(5);
		System.out.println("While Loop of 8: ");
		whileLoop(8);
		System.out.println("Do While Loop of 20: ");
		doWhileLoop(20);
		System.out.println("Recursion of 15: ");
		doWhileLoop(15);

	}
