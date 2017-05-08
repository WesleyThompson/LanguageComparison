## Comparison of C++ and Java
#### Team Members: Wesley Thompson

### 1. Language purpose/genesis
  * Why was the language created?
    * Java
      * Needed an architecture-neutral language for developing on multiple different embedded electronics or on the World-Wide Web. [Source](http://www.oracle.com/technetwork/java/javase/overview/javahistory-index-198355.html)
      
    * C++
      * Needed the performance of C but the easier large-scale development that classes / Object-oriented in Simula provided. [Source](http://www.cplusplus.com/info/history/)
      
  * What problems was the language trying to address?
    * Java
      * Supporting multiple platforms requires compiling a different version for each platform. Sometimes supporting different platforms requires major rewrites. Java instead allows "Write once, Run anywhere".

    * C++
      * Simula 67's new (at the time) Object Oriented paradigm was very useful for software development, but it was much slower than C and other low level solutions. C++ looked to combine the Object-Orientation of Simula with the speed and capability of C.

  * Is the language a reaction to a previous language or a replacement for another language?
    * Java
      * Reaction to Objective-C, C/C++
      * Sought to replace C/C++

    * C++
      * Reaction to Simula, and BCPL
      * Sought to replace C

### 2. Unique features of the language
  * Does the language have any particularly unique features?
    * Java
      * One of a few languages that runs on the Java Virtual Machine and that compiles to Java bytecode.
      
    * C++
      * Most features have been copied or done in a new way. C++ most unique feature is [Resource acquisition is initialization](https://en.wikipedia.org/wiki/Resource_acquisition_is_initialization).
      
### 3. Name spaces
  * How are name spaces implemented?
    * Java
      * Java packages
        * Creation: Directly mapped to a package directory.
        * Use: ``` using <name_of_namespace>; ```

    * C++
      * Creation: ` namespace <name_of_namespace> {  } `
      * Use: ` using namespace <name_of_namespace>; `

  * How are name spaces used?
    * Java
      * Name spaces are used to organize code as well as file/file-structure and to prevent name collisions.
      
    * C++
      * Name spaces are used to organize code into logical groups and to prevent name collisions.
      
### 4. Types
    * What types does the language support?
      * Java
        * Primitives: byte, short, int, long, float, double, boolean, and char
        * Also has java.lang.String class as support for character strings.

      * C++
        * Primitives: bool, char, int, float, double, void, wchar_t
        * Also has modifiers signed/unsigned and short/long which can be used as follows:
          * unsigned char, signed char, unsigned int, signed int, short int, unsigned short int, signed short int, long int, signed long int, unsigned long int, long double.

    * Are both reference and value types supported?
      * Java
        * Supports reference and value types, but is strictly pass-by-value, pass-by-reference isn't supported.
        
      * C++
        * Supports both reference and value types.
        
    * Can new value types be created?
      * Java
        * New value types are created via classes.
        
      * C++
        * Yes, through classes.
        
### 5. Classes
  * Defining
    * Java
      * ``` class Something {} ```
      * Access modifiers to class are optional

    * C++
      * ``` class Something {} ```
      * classes have no access modifiers

  * Creating new instances
    * Java
      * ` Something something = new Something(); `
      
    * C++
      * ` Something something; ` or ` Something *something = new Something(); `
      
  * Constructing/initializing
    * Java
      * ``` class Something {
                public Something() {
                    //some initialization
                }
            } ``` 
    * C++
      * ``` class Something {
                public:
                    Something();
            } 
            
            Something::Something() {
                //some initialization
            }``` 
  * Destructing/de-initializing
    * Java
      * Destructing is handled automatically as part of the Garbage Collection.
      * Can override the finalize() method to do extra destructing steps.
    * C++
      * ``` class Something {
                public:
                    ~Something();
            } 
            
            Something::~Something() {
                //some de-initialization
            } ```
        
### 6. Instance reference name in data type (class) this?  self?
    * Java
      * ``` class Something {
                string thing;
                public Something() {
                    //some initialization
                    this.thing = "a thing";
                }
            } ```
    * C++
      * ``` class Something {
                public:
                    string thing;
                    Something();
            } 
            
            Something::Something() {
                //some initialization
                this->thing = "a thing";
            } ``` 
            
### 7. Properties
  * Getters and setters...write your own or built in?
    * Java
      * Write your own
    * C++
      * Write your own
  * Backing variables?
    * Java
      * N/a
    * C++
      * N/a
  * Computed properties?
    * Java
      * N/a
    * C++
      * N/a
### 8. Interfaces / protocols
  * What does the language support?
    * Java
      * Interfaces
    * C++
      * No explicit support of interfaces
      * [Done through abstract classes](https://www.tutorialspoint.com/cplusplus/cpp_interfaces.htm)
  * What abilities does it have?
    * Java
      * Forces a class that implements an interface to have certain methods and leaves it up to the class to implement them
    * C++
      * N/a
  * How is it used?
    * Java
      * [Runnable](https://docs.oracle.com/javase/7/docs/api/java/lang/Thread.html) is a good example. Requires threaded object to implement the method run by implementing the interface Runnable.
    * C++
      * N/a
### 9. Inheritance / extension
  * Java
    * ```class Something {
      public void doThing() {}
    }  
    
    class SomethingElse extends Something {
      public void doOtherThing() {}
    }
    
    SomethingElse s = new SomethingElse();
    s.doThing();```
  * C++
    * ```class Something {
      public:
        void doThing() {}
    };
    
    class SomethingElse: public Something {
        void doOtherThing() {}
    };
    
    SomethingElse s;
    s.doThing();```
    
### 10. Reflection
  * What reflection abilities are supported?
    * Java
      * All typical reflection capabilities found via [java.lang.Class](https://docs.oracle.com/javase/8/docs/api/java/lang/Class.html)
    * C++
      * Not officially supported, but solutions can and have been created.
  * How is reflection used?
    * Java
      * Can be used to inspect classes at runtime to see their methods, constructors, properties, etc at runtime.
    * C++
      * N/a
### 11. Memory management
  * How is it handled?
    * Java
      * Garbage Collector
    * C++
      * Manual memory management
  * How does it work?
    * Java
      * Objects that pass out of reference are added to the garbage heap to be collected when a new object is created. The memory reclaims the memory as needed.
    * C++
      *  Manual allocation and deallocation. Or variables/objects pass out of scope and are deleted.
  * Garbage collection?
    * Java
      * Yes
    * C++
      * No
  * Automatic reference counting?
    * Java
      * No
    * C++
      * No
### 12. Comparisons of references and values
  * How are values compared? (i.e. comparing two strings)
    * Java
      * ` new String("test").equals("test") `
    * C++
      * ``` std::string string = "blah"
          if(string == "bleh") { . . . } ```
### 13. Null/nil references
  * Which does the language use? (null/nil/etc)
    * Java
      * null
    * C++
      * NULL
  * Does the language have features for handling null/nil references?
    * Java
      * [null ignore invocation](http://blog.joda.org/2007/01/java-7-null-ignore-invocation_9576.html)
    * C++
      * Nope manually check using an if statement.
### 14. Errors and exception handling
    * Java and C++ both use try-catch blocks to handle errors and exceptions.
### 15. Lambda expressions, closures, or functions as types
    * Java
      * Lambda expression: Create an anonymous  class that implements a functional interface
      * [Good Example](https://www.javatpoint.com/java-lambda-expressions) 
      ```interface Sayable{  
         public String say();  
         }  
         public class LambdaExpressionExample{  
         public static void main(String[] args) {  
         Sayable s=()->{  
             return "I have nothing to say.";  
         };  
         System.out.println(s.say());  
         }  
         }  ```
    * C++
      * Referred to as a lambda
      * [Good Example](https://msdn.microsoft.com/en-us/library/dd293608.aspx)
        * ```#include <algorithm>  
             #include <cmath>  

             void abssort(float* x, unsigned n) {  
                 std::sort(x, x + n,  
                     // Lambda expression begins  
                     [](float a, float b) {  
                         return (std::abs(a) < std::abs(b));  
                     } // end of lambda expression  
                 );  
             }  ```
  
### 16. Implementation of listeners and event handlers
    * Java
      * 
    * C++
      * 
### 17. Singleton
  * How is a singleton implemented?
    * Java
      * [implementation](http://www.journaldev.com/1377/java-singleton-design-pattern-best-practices-examples)
    * C++
      * [implementation](http://www.cplusplus.com/forum/general/43943/)
  * Can it be made thread-safe?
    * Java
      * yes
    * C++
      * yes
  * Can the singleton instance be lazily instantiated?
    * Java
      * [Yes](http://www.javapractices.com/topic/TopicAction.do?Id=34)
    * C++
      * [Yep](https://www.devarticles.com/c/a/Cplusplus/C-plus-plus-In-Theory-The-Singleton-Pattern-Part-I/4/)
### 18. Procedural programming
  * Does the language support procedural programming?
    * Java
      * Yes
    * C++
      * yes
### 19. Functional programming
  * Does the language support functional programming?
    * Java
      * [Yep](http://www.functionaljava.org/)
    * C++
      * [Yep](http://blog.madhukaraphatak.com/functional-programming-in-c++/)
### 20. Multithreading
  * Threads or thread-like abilities
    * Java
      * https://docs.oracle.com/javase/7/docs/api/java/lang/Thread.html
    * C++
      * http://www.cplusplus.com/reference/thread/thread/
  * How is multitasking accomplished?
    * Java
      * Don't understand the question
    * C++
      * Don't understand the question
