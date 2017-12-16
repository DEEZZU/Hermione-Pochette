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

int * a;
int arr[4];

sizeof(arr);
sizeof(a);

give your size preferecence to the interviewer
answer :
16
8

there is  fine line btw array name and pointer 
though array name is a can refence to first address

sizeof(*arr);
sizeof(14);
// sizeof(‘A’) <- most imp eg

array declaration
 int arr[10]; -> 40 bytes

the size should be const

int n;
cin>>n;
int arr[n]; // this doesn’t work in gcc 
// dynamic : after compilation 

in g++ error is not given : because memory size is inc so the compiler 
compiler dependent 

dynamic array creation 

int *arr= new int[n] ;
in c we have malloc 

memory allocation 
stack : function calling tym 
heap : dynamic memory allocation : extra setgment 
global : all prog var : data segment 

if the int arr[] is outside main , memory is given in data segment 
all globals get 0 value


int main()
{

int n ; in stack because in a function 
int * arr = new int[] : heap 

}


stack heap global 

sizeof(arr) : still gives pointer size 
new : allocates n bytes , gives first address to int* are 
int * arr is in stack 


initialization 
 values at the tym of declaration

int a[10]={1,2,3,4,5,….}; // initialisation -> compile 
a[0]=1; // assignment -> at tym of execution


int a[5]={1,2,3};
what is at 4 and 5 :

0
garbage
error
3,3
1,2
cant say
compiler error


the compiler would by default 0 

its a special case :

int a[5]={0};
all values get 0 
 int a[5] ={};
it gets all 0 no error 

int a[]={1,2}; <- allowed  // all static example 

int a[]{1,2,3};
this is new and valid initialisation in c++ newer version 
g++ 11 and g++14 works
 
SIZEOF(“A”) : 2

2 (STRINGS ARE ALWAYS NULL TERMINATED)
 COMPILER
1
4 


int a[‘a’]
sizeof(1); : 4 
sizeof(‘A’) : 4 : LOGICALLY :(MAC GIVES 1)
 
1) 4,4
 1,4
COMPILER


SIZEOF (DATATYPE)

int a[“a”] <- error


Element Access

a[0] <- first element
a[3/2] <- 2 nd element
a[3.0/2] <- error  (you can not return float )

a[-1] <- valid 
index should be integer

a[2]= *(a+2)
a[-1]=*(a+(-1))
^ this gives garbage value 

java gives array out of bound exception 
it is a possibility that it gives runtime error
segmentation fault  : u have moved out of the memory 
 

if u allocate using new : but a good practice is to deallocate yourself : delete 

delete[] a; <- how does operating system know how much size is to be deleted : just previous location has  size stored 
and marks it free 

^ dynamic deallocation 
int * a ? what happens to it : it might get the dangling pointer or if the compiler is optimised it might get null 

int * a does not get deleted but the heap is notified that it is free 
int * a is itself a static variable in memory

try :

int arr[5];
delete[ ] arr;

^ check for yourself
arr=&a; <- does obviously give error

memory leak : memory was allocated but os was not notified that it is free

it is not accessible

suppose u returned without deleting 

eg :

int fun()
{
int *arr=new int[5];
return 1;

} 

memory leak 

in c there is no call by reference

call by value is in c 

in c++ : difference btw call by reference and call by pointer 

CALL BY VALUE :

doesn’t exchange value

call by reference:

aliases of the variables 
no new memory is allocated 


CALL BY POINTER :


POINTER HAS NEW MEMORY ALLOCATED  FOR STORING THE ADDRESS OF THE A AND B 

IT IS CALL BY VALUE BECAUSE VALUE OF ADDRESS IS BEING COPIED 


practical :
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


TEMPLATES CAN BE USED TO SEND SIZE 

VOID FUCNT(INT ARR[])
{
INT S= SIZE OF(ARR )/SIZE OF(ARRO)
}


WE CAN NOT USE ARRAY AS AN ASSIGNMENT 
IT IS CONSTANT 

