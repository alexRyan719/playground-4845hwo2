# Objects

Strings are often lumped in with primitive variables, but they are actually what we consider "objects." Objects are more complex variables that are capable 
of storing multiple values. In the case of strings, you're storing and using an array of chars (characters or letters). You can use arrays to store all the types 
of primitive variables. 

# Constructors

For any object in Java, it needs a Constructor to build it to specifications. 

<!-- insert example of constructor -->

# Arrays

Arrays are groups of variables. As mentioned above, Strings are a good example of an array of chars. The indexing for arrays starts at 0. Think of indexing as 
how many spaces away from the initial space are we. At index 0 of the string "Hello" is 'H'. Also, notice how I used double quotes for multiple chars and single
quotes for a single char. 

In Java, arrays need to be declared with a finite length. 

<!-- insert example -->

# ArrayLists

Array lists are more complex types of arrays. They are dynamically sized, so you don't have to worry about it filling up and causing an error. However, this adds
to the overhead. This means that by calculating a new size based on how large the current array list is becoming costs computational power, and time. 

# 2D Arrays

One of the best examples of a 2D array would be an image. An image file has a width and a height, then is filled in with pixel values. This forms a 2 Dimenstional
grid. 

# Binary Search Trees

Binary search trees are a tad complex, but worth understanding. The idea is to sort data and then use a sorted structure to cut down on how many items need to be
searched before the desired data is found. 

# Graphs

Graphs are much more complex ways to store data. However, this complexity leads to being very dynamic and efficient. Graphs consist of nodes and edges that connect
those nodes. Each node will have a list of the edges it has connecting it to other nodes. 
