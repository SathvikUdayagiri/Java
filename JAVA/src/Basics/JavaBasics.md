# Java Basics

## Data Types and there Memory.

1. Byte: 1 byte -> 8 bits -> -128 to 127
2. Short: 2 bytes -> 16 bits -> -32768 to 32767
3. Integer: 4 bytes -> 32bits -> -2,147,483,648 to 2,147,483,647 (we can also add an under score("_") in between numbers so that counting the zeros will be easy).
4. Long: 8 bytes we have to specify l for long.
5. Float: 4 bytes we have to add f at last, as default value is double.
6. Double: 8 bytes.
7. Character: American Standard Code for Information Interchange.

### Implicit conversion

`double double_number_2=5;`

## Naming Conversions

### Camel Casing Rule

#### Variable:

eg: sname, stockprice,...(All small letters)

#### Class: Noun

eg: Student,Person,Computer,HashMap(Capital letter at starting of every word)

#### Interface : Adjective

Runable,Readable, Remote...(Capital letter at starting of every word and most of the interfaces end with able) 

#### Method: Verb

eg: actionPerformed,run,print(Capital letter at starting of every word from 2nd word)

#### Constant:

PI,DENSITY,MAX_PRICE(Every letter is capital and there is a underscore(_) in between every word)

#### Examples:

Variable: abc
Constant: ABC
Constructor: Abc()
Method: abc()
Interface: Stretchable

## Operators

### Arithmetic : +,-,*,/,%

### Bitwise : <<,>>

### Relational : <,>,<=,>=.==,!=

### Logical: 

## Short Hand Operator: 

++(Increment operator),--(Decrement Operator),+=,-=,*=,/=
++n(pre Increment)
--n(Post Increment)

## Selection Statements

### 1.if:

    if(condition)
    {
        if condition is true this block runs
    } 
    else if(condition 2)
    {
        if condition 2 is true this block runs
    }
    else
    {
        if condition and condition 2 is flase this block runs
    }

### 2.ternary : 

    condition ? expr1 : expr2 (if condition is true then expr1 else expr2)

eg: n=5>6?5:6

### 3.switch:

    switch (key) 
    {
        case value: 
        run this block;
        break;
    default:
    default statement;
    }

we can also use strings in switch(in place of key)

## Iteration

### 1.for:

    for(i=0 (Initilization); i<5 (Condition); i++ (Increment) )
    {
    statement;
    }

### 2.while:

    i=0 (Initilazion)
    while(i<=5 (Condition))
    {
    statement;
    i++ (Increment)
    }

### 3.do while : 

executes at least once and then check the condition and run till the condition is false.

    i=0; (Initilization)
    do
    {
    statement
    i++; (Incrementation)
    }
    while(i<=5 (Condition));

### 4.for-each:

#### ctrl+shift+f for formatting the code in "Eclipse".

## Break,Continue and Exit.

### break : it will break/ends the loop or it comes out of the loop. 

### continue : it will skip the statements below it continues the next iteration of the loop or it will skip the iteration.

### exit : it exits from the entire program.

## OOP's concept

    class Calc
    {
        int num1;
        int num2;
        int result;
        public void perform() //Access modifier.
        {
            result=num1+num2;
        }
    }
    public class ObjectDemo
    {
        public static void main(String[] args)
        {
            Calc obj; // this is not an object it is just a reference to class Calc
            obj=new Calc() // new is responsible to allocate the memory , "new Calc()" is Object , new is to create an object, it stores in Heap Memory
            obj.num1=3 // obj is reference
            obj.num2=5;
            Sysout.out.println(obj.result); // it prints 0 as we haven't assigned any value
            obj.perform();
            System.out.println(obj.result);
        }
    }  

### Space of an object is defined by the constructor

### default values for int variables is 0

### Constructor: 

it is a member method which has the same name as class name.it will never return anything so no return type but access modifier is required.space required by an object is given by constructor, it will be used to allocate the memory.it can be also used to initialize the values,constructor is called automatically when an object created.We can have more than one constructor with different signature and it is called constructor overloading it is a part of polymorphism.

#### Constructors are two types default constructor an parameterized constructor.

### Function Overloading and function Overriding:

### This Keyword: 

Local Variable always shadows the instance variable or class variable. So we use "this" keyword, this represents to the current object or current instance.

### class loader memory:

The Java ClassLoader is a part of the Java Runtime Environment that dynamically loads Java classes into the Java Virtual Machine. The Java run time system does not need to know about files and file systems because of class loaders. Java classes aren’t loaded into memory all at once, but when required by an application.At this point, the Java ClassLoader is called by the JRE and these ClassLoaders load classes into memory dynamically.

### Static:

#### static variable:

if we make an variable static then it is same for all objects,like all objects have same value, and after making it static it will not store in heap memory it will store in class loader memory.and as the static variable is same for all the objects we need not to use an object to assign the value of the static variable, we can use class the class name to assign the value.we can use both class name or object name to assign and access the variable

#### static method:

we can also make method static, main is static as we can call it without an object.we don's need an object to call static methods.

#### static block:
 
it is a special block in java where it doesn't matter how many objects are created it executes only once. and it is used for initializing the static variables.we can use constructor to initialize non-static variables and static block to initialize static variables.constructor executes when an object is created (or) when we create an object and static block executes only when we load a class, The clas will load only once.class loads first then only we can create an object, so static block executes first and then constructor executes.if we create more than one static blocks then sequence matters, like top to bottom.

#### Static Class: we will discuss static class in Inner classes

##### Static variable are those variables which are same for all the objects and non static-variables are those variables which are different for all the objects.

##### we can access a non-static variable inside a static block or static function(like main function which is static).

syntax:

    static
    {

    }

## Access modifier:

## Inner class:

Inside a class we can create a variables and methds.
we can also create a class inside a class
and they are called member variable, member method and member class.

### we can create an inner object we have to use `outer.inner obj=obj.new inner();` in order to use the inner class, the class itself we have to use the outer class, but in order to create an object of inner class we need to use object of outer class.

inner class is used for 

#### we can also have static class.

##### if we make an inner class as static then we don't need to an object to create the object of it.`Outer.Inner obj=new Outer.Inner()`.

### In Inner class we have:

#### member class

#### static class

#### --> Anonymous class

## Array: It is Collection of Elements. And Index starts from 0.

1. 1D Array
2. 2D Array
3. Jagged Array:

### --> Arrays are stored in "Heap Memory".

### --> Arrays when initialized by default the values inside the array will be initialized to 0.

    int nums[]=new Int[size]
    int nums[]={8,12,76,54};

### --> Enhanced for loop

#### for 1D arrays

    for(int k : a) (a is an array)
    {

    }

#### for 2D arrays

    for(int k[] : d)
    {
        for(int l : k)
        {

        }
    }

## Varrays:

Variable arguments or variable lenght arguments.

    public int add(int ... n)
    {
        int sum=0;
        for(int i : n)
        {
            sum=sum+i;
        }
        return sum;
    }