Tell me about yourself and waht are you currently working on

climb stair - 
1. You are given a number n representing number of stairs in a staircase.
2. You are standing at the bottom of staircase. You are allowed to climb 1 step, 2 steps or 3 steps in one move.
You need to get the list of all paths that can be used to climb to the top
what will be your approach
3 stairs
111 12 21  3

reverse a string using recursion
n raised to k using recursion

--------------------------------------------------------------------------------------Core java


Name some OOPS Concepts in Java?
	Java is based on Object Oriented Programming Concepts, following are some of the OOPS concepts implemented in java programming.

		Abstraction
		Encapsulation
		Polymorphism
		Inheritance
		Association
		Aggregation
		Composition


What do you mean by platform independence of Java?
	Platform independence means that you can run the same Java Program in any Operating System. For example, you can write java program in Windows and run it in Mac OS.


What is JVM and is it platform independent?
		Java Virtual Machine (JVM) is the heart of java programming language. JVM is responsible for converting byte code into machine-readable code. JVM is not platform-independent, that’s why you have different JVM for different operating systems. We can customize JVM with Java Options, such as allocating minimum and maximum memory to JVM. It’s called virtual because it provides an interface that doesn’t depend on the underlying OS.

How JVM works in Java ?  (https://www.javainterviewpoint.com/java-virtual-machine-architecture-in-java/)
		Class Loader Subsystem
		Runtime Data Area
		Execution Engine
		
		
		
try without catch is it allowed?
in what scenerio finally wis not executed? - - 
 -- when system.exit(1) in try block
 -- exception is occuered in finally

    public static void main(String[] args) {
        try {
            System.out.println("abc");
            if (1 == 1)
                throw new Exception();
            return;
        } catch (Exception e) {
            System.out.println(e);
            return;
        } finally {

            System.out.println("closing");

        }
    }
will finally get executed?
if exception occurs	
	
What is try-with-resources in java?
		One of the Java 7 features is the try-with-resources statement for automatic resource management. Before Java 7, there was no auto resource management and we should explicitly close the resource. Usually, it was done in the finally block of a try-catch statement. This approach used to cause memory leaks when we forgot to close the resource.

		From Java 7, we can create resources inside try block and use it. Java takes care of closing it as soon as try-catch block gets finished. Read more at Java Automatic Resource Management.
		
		
Java try with resources benefits
			Some of the benefits of using try with resources in java are;

			More readable code and easy to write.
			Automatic resource management.
			Number of lines of code is reduced.
			No need of finally block just to close the resources.
			We can open multiple resources in try-with-resources statement separated by a semicolon. For example, we can write following code:

			try (BufferedReader br = new BufferedReader(new FileReader(
							"C:\\journaldev.txt"));
							java.io.BufferedWriter writer = java.nio.file.Files.newBufferedWriter(FileSystems.getDefault().getPath("C:\\journaldev.txt"), Charset.defaultCharset())) {
						System.out.println(br.readLine());
					} catch (IOException e) {
						e.printStackTrace();
					}
			When multiple resources are opened in try-with-resources, it closes them in the reverse order to avoid any dependency issue. You can extend my resource program to prove that.
			Java 7 has introduced a new interface java.lang.AutoCloseable. To use any resource in try-with-resources, it must implement AutoCloseable interface else java compiler will throw compilation error.
			
			
			
			
			---------------------------------------------------------------------------Collection
			
			
			
Java provides two interfaces to sort objects using data members of the class: 
 

		Comparable ->Default sorting
		Comparator --> multiple data member
		
		Lets say i have List of 6 Employee class{
			String name
			int age
			BigInt salary;

			}
			
			Name   age	salary
			A		30		50k
			A 		25		40k
			B		27		45k
			B		27		40k
			C		30		55k
			C		25		35k
			
			i want to sort by name then by age then by salary- > like in sql we have order by name age salary
			can we doo this by comparable and comparator
			give me the approach and 
			write it down on paper the compareTO function.  and  read it out to me
			dont use java 8
			
			
1. Have you used set list queue and map interface
2. Why Map interface doesn’t extend Collection interface?
3. INternal working of hashmap
4.


--------------------------------------------------------------					-Multithreading

1. do you knwo states of thread
2. executor service
3. future and callable interface
4. concurrency and parallelism

		
* 	concurrency- > 4 thread and single core  vs 4 thread and 4 cores
* 			parallelism->	(fork/join) list of string a,b,c,d and need to do uppercase
*

------------------------------------------------------------------------------Serialization deserialization --clonable 
1. what is serialization and deserialization
2. how will you serialize obj and deserialize obj
3. transient keyword- ? part of obj to be serialize

* int i=100; int j=200;	100………………………….200
* transient int i=100;
* int j=200;	0………………………….200
* transient int i=100;
* transient static int j=200;	0………………………….200
* transient final int i=100;
* transient int j=200;	100………………………….0
* Transient final int i=100;
* transient static int j=200;	100………………………….200

* shallow copy and deep copy
*

----------------------------------------------------------------------------desing pattern
1. singleton? where it is used 
2. looging
3. caching 
4. db connection

1. readResolve();  when we serialize single ton and deserialize single ton then 2 instance is created to avaoid that 
2.


		
----------------------------------------------------------------------------String
* String string buffer string builder
* why string immutable 
* intern keyword-
* String s1="abhi
* String s2 ="abhi"   
* s1==s2?
* string s3 = new String("Abhi")
* if s1==s3?

1. Equals and hahscode

	
=---------------------------------------------------------------------jaava features 

java 8 features
lastest java used and its features


--------------------------------------------------------------Spring Frame work

1. What is DI
2. 
3. @Autowired
4. by name 
5. bytype 
6. construcotror
7. @Component
8. @Repository

1. Let say you have configuured jdbc in your spring project and  jdbc exception occurs in spring then how it gets converted in to spring sxception
2. How conponent scanning takes place in spring and spriongboot
3. @Service
4. @Contriller vs @restcontroller
5. @ControlelrAdvice
6. @Qualifier
7. @transaction
8. and isolation level

profiles in spring boot
scope of bean - singleton prototype request,session

setter vs constructor injection?


AOP
JMS JDBC

MVC
what is use of dispatcher servlet

------------------------------------------------------------Spring BAtch


------------------------------------------------------------Spring Integration


------------------------------------------------------------SOA


------------------------------------------------------------ SOAP AND REST

difference between put and post

https://www.javainterviewpoint.com/jax-rs-pathparam-example/
------------------------------------------------------------UI
HTML
CSS
JS 
Filter then Map
const orders = [
  { quantity: 2, item: { name: 'T-Shirt', price: 25 } },
  { quantity: 1, item: { name: 'Keyboard', price: 75 } },
  // Maybe there was a bug and a order with a null `item` ended up in the database!
  { quantity: 2, item: null }
];
i wnat only vzlid order list

const orderedItemNames = orders.
  filter(order => order.item != null).
  map(order => order.item.name);


 Explain call(), apply() and, bind() methods.
12. What is currying in JavaScript?


* Angular
* which angular version you have used
* when data json data is passed from angular to java , how it is getting passes to and fro?
*

------------------------------------------------------------plsql
* dml ddl dcl
* normalization
* isolation level
* lets say you have list of employee with name age salary- i want employee with 2nd largest salary (dont use order by)
* .
* 
* ------------------------------------------------------------Buildtool
* Which build too you have used?


* -----------------------------------------------------Project related question
* Explain your project along with all the components
* Explain the Architecture of your Java Project
* Versions of different components used
* Which are the biggest challenges you have faced while working on Java project?
* ----------->angular app integration cannot add backend jar so for front end  , multiple save connections so used pipeline
* Which is your biggest achievement in the mentioned Java project?
* Did you stuck in a situation where there was no path ahead, how you handled that case?
* Which is your favorite forum to get help while facing issues?
* How you coordinate with the client in case of any issues?
* How you educate your client for the problems which they are not aware of?
* Do you have any experience in pre-sales?
* What were your roles and responsibilities in last Java project?
* Which design pattern did you follow and why?
* Best practices in Java development that you followed?

* i am done
* do you have any question
* i need to provide the review
*
			
			
