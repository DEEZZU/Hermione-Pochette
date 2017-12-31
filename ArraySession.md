## Arrays

Session By :  Shagun Aggarwal 

Date : 16 November 2017 

----

### The Basics 


**_What are data structures ? What is the importance of  Data Structures ?_**

```
Data Structures :
Used for organisation of data

Importance : 
Consider and example; we have a library and then there is some market of book ; 
(assuming all contraints that they have same amount of informationa and etc) ;
one prefers library just because of the 
             1. Ease of Search
             2. Reduced time of Search 
             3. Availability can be tested faster
Here, library is a data structure which stores books in a particular order or organisation.
```

**_What happens when u declare "int a"?_**

```

A Memory gets allocated for the variable a.

Basically, when u declare a variable , u want to reserve a (x amount of) memory which 
u want to access. Now, it is rather difficult to remember the memory's address so u name it . 

So when u write "int a" , 4 bytes of memory are reserved and whenever u write "a" ,  
the computer understands that u are talking about that memory.

```

**_Simplest Data Structures_**

```

The primitive data types are the simplest data structures.
Also known as : Atomic data types. 
Some of the fixed ones which appear in most languages : int , float/real/double, bool , char etc.

```

----

### Next Comes :  ARRAY

**_What are Arrays?_**

```

* Collection of Same data type  
* Continuous memory allocation
* Best One : Contigous Homogenous Collection of Data Structures 

```

**_Indexing in Array_**

```

Use of Continuous Allocation : it allows random-access. 
indexing usually starts with 0 (majorly) 
but exceptions are there (eg in r : 1)
The indexes increases by +1.
For algorithms we assume the starting from 1.

```

**_Understanding Size of Array_**

Consider an Example:

```c++

int * a;
int arr[4];

cout << sizeof(arr) ;
cout << sizeof(a) ;

```

##### Output :

(Word of caution: give your size preferences to the interviewer)
 ```
 16
 8
 ```

**_Array Name and Pointer_**

There is a fine line between Array Name and Pointer ; though array name can reference to first address; 
it is not a pointer.

```c++
cout << sizeof(*arr);
cout << sizeof(14);
cout << sizeof(‘A’);      //     <- most imp eg
```

When you output the above 3 line of Codes , you get :

```
8 
4
1 (or 4)
```

Output Explaination :

```

Well ! Assuming the size of pointer be 8 bytes , we get an 8 when we print the pointer to the base address of Array.
Further, 14 is an Integer so we get 4 Bytes for it.
And the last one would give 1 on Clang (Mac Xcode) for its a Character, BUT it gives 4 Bytes on G++14 for 'A' is an
Ascii code which is an Integer and hence 4 bytes.

```

**_Array Declaration_**


* Static Declaration , using constant size :

```c++

base_type_of_array array_name[ array_size_in_constant ] ;     //      -> Size = array_size_in_contant X base_type_of_array

// Following are some valid declarations 

int arr[10];     //     -> 40 bytes
int arr['A'];    //     -> 260 bytes
```

** It is important to note that the size should be constant **

* Dynamic Declaration , using user input :

```c++

// Type 1 
int n ;
cin >> n ;
int arr[n] ;        // this doesn’t work in gcc 
                    // dynamic : after compilation 
                    // in g++ : error is not given : because memory size is inc so the compiler 
                    // compiler dependent 


// Type 2
int *arr = new int[n];
             
```

** In C we have 'malloc' keyword **

----


#### Memory Allocation


**_Segments and Memory Map_**

Memory is devided into 4 segments :
  
  *Code Segment*

  *Data Segment*

  *Stack Segment*

  *Extra Segment*


**Understanding the mapping of memory allotted to Program :**

![image of Memory allotted to a program](https://github.com/DEEZZU/Hermione_Pochette/blob/master/Images/memoryMap.jpg)


```
As given above , a program gets memory , and it has four bifurcation :
  *Stack
  *Heap
  *Global Variables
  *Program Code
```

**1. Stack :**
     
     used at the tym of function calling 
     is in the "Stack Segment" of the memory.
     
     
**2. Heap :**
     
     dynamic memory allocation 
     in "extra setgment" 
     
     
**3. Global :**
    
     all program variables 
     in "data segment"
     Consider : if the  declaration "int arr[];" is outside main() (considering c++), memory is given in data segment 
     all global variables get 0 value

**4. Program Code:**

      code of the program 
      in "code segment"
      

```c++

  int arr[maxSize];                  // -> in Global Variable
  
  int main()
  {

    int n ;                          // -> in Stack ( because main() is a function )
    int * arr = new int[n];          // -> in Heap 
    
  }
  
```
 
``` 
*Some Important Noteworthy Points in the example :*
   
If i print ;

        sizeof(arr);  
        
this would still give pointer size as output.

Why ?
The operator , "new" , it allocates n bytes , gives first address to int* "arr" .
    
Now , an important point to be noted , where is int* arr ?? 
"int* arr is in stack" and , the array of n bytes is in heap !!!
```
____

**_Array Initialization_** 

```
values at the tym of declaration
these are assigned at the time of compilation
```

```c++

int a[10] = {1,2,3,4,5,….};         // initialisation
a[0]=1;                             // this is assignment -> value given at time of execution


int a[5]={1,2,3};                   // this statement initializes first 3 positions but 
                                    // for position 4 and 5 we get '0'
```


_Ques: What is at a[4] and a[5] ?
      a) 0
      b) garbage
      c) error
      d) 3,3
      e) 1,2
      f) cant say
      g) compiler error_

Ans : **a)** , reason : The Compiler would by default set them to 0. 


```c++

int a[5] = {0} ;                   // all values get 0 
int a[5] = {} ;                    // it gets all 0 ; no error 
int a[] = {1,2} ;                  // all static example <- allowed
int a[]{1,2,3};                    // this is new and valid initialisation in c++ newer version 
                                   // g++11 and g++14 works

``` 


_Ques : SIZEOF(“A”) ? 
       a) 2 
       b) 1
       c) 4_
       
Ans : **a)** reason : STRINGS ARE ALWAYS NULL TERMINATED


_Ques :int a[“a”] ?_
  
Ans : **This generates error.**


**_Element Access_**

```c++
a[0];                                 // <- first element
a[3/2];                               // <- second element
a[3.0/2];                             // <- error (you can not return float )
a[-1];                                // <- valid 

```

```
Important points to note:

Index should be integer 

What does a[x] means ? 
Consider an example : 
         a[2]= * (a+2);
         a[-1] = * (a+(-1));          // this gives garbage value 
                                      // java gives array out of bound exception 
                                      // it is a possibility that it gives runtime error
                                      // segmentation fault  : u have moved out of the memory 
```

----

**_Dynamic Deallocation_**

So when u declare int * a ? what happens to it : it might get the dangling pointer or if the compiler is optimised it might get null 
if u allocate using new : but a good practice is to deallocate yourself : delete 

delete[] a; <- how does operating system know how much size is to be deleted : just previous location has  size stored 
and marks it free 

^ dynamic deallocation 


int * a does not get deleted but the heap is notified that it is free 
int * a is itself a static variable in memory

try :

int arr[5];
delete[ ] arr;

^ check for yourself
arr=&a; <- does obviously give error

----

**_Memory Leak_**

* A memory leak occurs when the memory was allocated but os was not notified that it is free now 
* and since nobody freed that area , it is not accessible
* Example : suppose u returned without deleting a pointer assigned memory in the function 

```c++

int fun()
{
int *arr=new int[5];
return 1;
} 
```

----

**Call By Value/ Reference/ Pointer** 

* In c : there is no call by reference, only call by value and pointer.
* In c++ : We have call by value , call by reference and call by pointer .

Understanding the difference ;

CALL BY VALUE :
*actual arguments' values get copied into the formal ones

CALL BE REFERENCE :
*aliases of the variables 
*no new memory is allocated, as in the actual arguments are just another alias of the formal argument variable 


CALL BY POINTER :
*pointer variables are declared 
*they capture the address of the variables 
**_IT IS CALL BY VALUE BECAUSE VALUE OF ADDRESS IS BEING COPIED_** 

```c++

// Declaration of the three types of call 

int fun(int a, int b);
int fun(int &a , int &b);
int fun(int* a , int* b);

```

----



TEMPLATES CAN BE USED TO SEND SIZE 

VOID FUCNT(INT ARR[])
{
INT S= SIZE OF(ARR )/SIZE OF(ARRO)
}


WE CAN NOT USE ARRAY AS AN ASSIGNMENT 
IT IS CONSTANT 

```C++
    
    int a['A'] = {0};
    int ab = 'A';
    num1=5;
    num2=6;
    
    int *a1=&num1;
    int *b1=&num2;
    int temp=0;
    
    temp=(*a1);
    
    *a1=*b1;
    *b1=temp;
    cout  << num1 << num2 ;
    cout << sizeof((int)('A')) << " " << sizeof("A") << " " << ab << endl;
cout << "sizeof(a)" << sizeof(a)/sizeof(a[0]) ;

```    
