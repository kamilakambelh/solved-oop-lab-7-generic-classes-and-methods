Download Link: https://assignmentchef.com/product/solved-oop-lab-7-generic-classes-and-methods
<br>



<ol>

 <li><strong> Get familiar with generic types </strong>Given the following class</li>

</ol>

public class MyPair&lt;T, U&gt; { public final T Fst; public final U Snd;

public MyPair(T fst, U snd) { this.Fst = fst; this.Snd = snd;

}

public String toString() { return “(” + Fst + “, ” + Snd + “)”; }

}

<ol>

 <li>In a new source file, write a program that includes this declaration and also a class with an empty Main method. Compile it to check that the program is well-formed.</li>

 <li>Declare a variable of type MyPair&lt;String, Integer&gt; and create some values, for instance new MyPair&lt;String, Integer&gt;(“Anders”, 13), and assign them to the variable.</li>

 <li>Declare a variable of type MyPair&lt;String, Double&gt;. Create a value such as new MyPair&lt;String, Double&gt;(“Phoenix”, 39.7) and assign it to the variable.</li>

 <li>Can you assign a value of type MyPair&lt;String, Double&gt; to a variable of type MyPair&lt;String, Integer&gt;? Should this be allowed?</li>

 <li>Declare a variable grades of type MyPair&lt;String, Integer&gt;[], create an array of length 5 with element type MyPair and assign it to the variable. Create a few MyPairs and store them into grades[0], grades[1] and grades[2].</li>

 <li>Use the foreach statement to iterate over grades and print all its elements. What are the values of those array elements you did not assign anything to?</li>

 <li>Declare a variable appointment of type</li>

</ol>

MyPair&lt;MyPair&lt;Integer, Integer&gt;, String&gt;

and create a value of this type and assign it to the variable.

What is the type of appointment.Fst.Snd? This shows that a type argument may itself be a constructed type.

<ol>

 <li>Declare a method Swap() in MyPair&lt;T, U&gt; that returns a new value of type MyPair in which the components have been swapped.</li>

 <li><strong> Differences between Object, generic and generic raw types</strong></li>

</ol>

In JAVA, there is a Map data structure that helps developers to link a key to a value.

Read about Map in

<ul>

 <li><a href="https://www.geeksforgeeks.org/map-interface-java-examples/">https://www.geeksforgeeks.org/map</a><a href="https://www.geeksforgeeks.org/map-interface-java-examples/">–</a><a href="https://www.geeksforgeeks.org/map-interface-java-examples/">interface</a><a href="https://www.geeksforgeeks.org/map-interface-java-examples/">–</a><a href="https://www.geeksforgeeks.org/map-interface-java-examples/">java</a><a href="https://www.geeksforgeeks.org/map-interface-java-examples/">–</a><a href="https://www.geeksforgeeks.org/map-interface-java-examples/">examples/</a></li>

 <li><a href="https://www.geeksforgeeks.org/java-util-hashmap-in-java/">https://www.geeksforgeeks.org/java</a><a href="https://www.geeksforgeeks.org/java-util-hashmap-in-java/">–</a><a href="https://www.geeksforgeeks.org/java-util-hashmap-in-java/">util</a><a href="https://www.geeksforgeeks.org/java-util-hashmap-in-java/">–</a><a href="https://www.geeksforgeeks.org/java-util-hashmap-in-java/">hashmap</a><a href="https://www.geeksforgeeks.org/java-util-hashmap-in-java/">–</a><a href="https://www.geeksforgeeks.org/java-util-hashmap-in-java/">in</a><a href="https://www.geeksforgeeks.org/java-util-hashmap-in-java/">–</a><a href="https://www.geeksforgeeks.org/java-util-hashmap-in-java/">java/</a></li>

 <li><a href="https://www.tutorialspoint.com/java/java_hashmap_class.htm">https://www.tutorialspoint.com/java/java_hashmap_class.htm</a></li>

</ul>

As we want to reimplement the Map class, implement a class named MyMap to manage (store and get back) any object by its ID.

<ul>

 <li>User can put an object <strong><em>obj</em></strong> to a Map <strong><em>m</em></strong> by calling</li>

</ul>

<em>m.put(obj.getID(), obj);</em>

<ul>

 <li>User can get back an object from the map <strong><em>m</em></strong> by invoking</li>

</ul>

<h1>m.get(id);</h1>

<ol>

 <li>Implement the MyMap in two different ways:

  <ol>

   <li>Use Object as the type for both the Key and the Value parameters of the <strong><em>put</em></strong> and <strong><em>get </em></strong>methods</li>

   <li>Use generic type</li>

  </ol></li>

 <li>With your implementations, write a main function to

  <ol>

   <li>Test these two implementations</li>

   <li>To show advantage of generic type over Object</li>

   <li>To show advantage of parameterized type over generic raw type</li>

  </ol></li>

</ol>

Reference: textbook “Java How to Program”, chapter 20