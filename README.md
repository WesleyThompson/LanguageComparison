### Comparison of C++ and Java
#### Team Members: Wesley Thompson

* Language purpose/genesis
  * Why was the language created?
    * Java
      * Needed an architecture-neutral language for developing on multiple different embedded electronics or on the World-Wide Web.
      
    * C++
      * Needed the performance of C but the easier large-scale development that classes in Simula provided.
      
  * What problems was the language trying to address?
    * Java
      * Supporting multiple platforms requires compiling a different version for each platform. Sometimes supporting different platforms requires major rewrites.

    * C++
      * Developing large scale software is difficult in low-level languages and many class oriented solutions at the time were too slow.

  * Is the language a reaction to a previous language or a replacement for another language?
    * Java
      * Reaction to Objective-C
      * Sought to replace C++

    * C++
      * Reaction to Simula, and BCPL
      * Sought to replace C

* Unique features of the language
  * Does the language have any particularly unique features?
    * Java
      * One of a few languages that runs on the Java Virtual Machine.
      * Compiles to Java bytecode.
      
    * C++
      * [Resource acquisition is initialization](https://en.wikipedia.org/wiki/Resource_acquisition_is_initialization)
      
* Name spaces
  * How are name spaces implemented?
    * Java
      * Java packages
        * directly mapped to file

    * C++
      * namespace <name_of_namespace> {  }

  * How are name spaces used?
    * Java
      * Name spaces in java allow multiple classes to have the same name but also dictates the file location of the class.
      
    * C++
      * Name spaces are used to allow multiple classes to have the same name by being in different name spaces.
      
* Types
    * What types does the language support?
      * Java
        * Byte
        * Short
        * Integer
        * Long
        * Float
        * Double
        * Boolean
        * Character
        * Enumeration

      * C++
        * Boolean
        * Character
        * Integer
        * Float
        * Double
        * Wide Character
        * Enumeration

    * Are both reference and value types supported?
      * Java
        * Yes
        
      * C++
        * Yes
        
    * Can new value types be created?
      * Java
        * Yes, through classes
        
      * C++
        * Yes, through classes
        
* Classes
  * Defining
    * Java
      * ``` class Something {} ```
      * access modifiers to class are optional

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
            } 
            
        ``` 
    * C++
      * ``` class Something {
                public:
                    Something();
            } 
            
            Something::Something() {
                //some initialization
            }
        ``` 
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
            }
        ``` 
* Instance reference name in data type (class) this?  self?
    * Java
      * ``` class Something {
                string thing;
                public Something() {
                    //some initialization
                    this.thing = "a thing";
                }
            } 
        ```
    * C++
      * ``` class Something {
                public:
                    string thing;
                    Something();
            } 
            
            Something::Something() {
                //some initialization
                this->thing = "a thing";
            }
        ``` 
* Properties
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
* Interfaces / protocols
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
      * [Runnable](https://docs.oracle.com/javase/7/docs/api/java/lang/Thread.html) is a good example. Requires threaded object to implement the method run by implementing the interface Runnable
    * C++
      * N/a
* Inheritance / extension
* Reflection
  * What reflection abilities are supported?
    * Java
      * https://www.javatpoint.com/java-reflection
    * C++
      * Not supported
  * How is reflection used?
    * Java
      * Accessing what a class is etc.
      * Accessing a classes members etc.
    * C++
      * N/a
* Memory management
  * How is it handled?
    * Java
      * Garbage Collector
    * C++
      * Manually
  * How does it work?
    * Java
      * Objects that pass out of reference are added to the garbage heap to be collected when a new object is created
    * C++
      * Allocation and deallocation
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
* Comparisons of references and values
  * How are values compared? (i.e. comparing two strings)
    * Java
      * 
    * C++
      * 
* Null/nil references
  * Which does the language use? (null/nil/etc)
    * Java
      * 
    * C++
  * Does the language have features for handling null/nil references?
    * Java
      * 
    * C++
      * 
* Errors and exception handling
    * Java
      * 
    * C++
      * 
* Lambda expressions, closures, or functions as types
    * Java
      * 
    * C++
      * 
* Implementation of listeners and event handlers
    * Java
      * 
    * C++
      * 
* Singleton
  * How is a singleton implemented?
    * Java
      * 
    * C++
      * 
  * Can it be made thread-safe?
    * Java
      * 
    * C++
      * 
  * Can the singleton instance be lazily instantiated?
    * Java
      * 
    * C++
* Procedural programming
  * Does the language support procedural programming?
    * Java
      * 
    * C++
      * 
* Functional programming
  * Does the language support functional programming?
    * Java
      * 
    * C++
      * 
* Multithreading
  * Threads or thread-like abilities
    * Java
      * 
    * C++
      * 
  * How is multitasking accomplished?
    * Java
      * 
    * C++
      * 
