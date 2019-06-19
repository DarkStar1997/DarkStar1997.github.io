- High Performance Computing

Rohan Mark Gomes

3rd Year, Sec – A, Roll-45

Exam roll: 10400116125

Institute of Engineering & Management

Seminar Lab - CS681

Contents

- Certificate of Approval

- ACKNOWLEDGEMENT

- Contents

- Abstract

- Introduction

- Importance of HPC in the Job Market

- Languages used in HPC

Fortran

C

C++

Importance of C++ in HPC

Other languages

- Important aspects of HPC

Parallel Programming

GPU Programming

Memory Considerations

Interpreted v Compiled languages

Looping speed

String Concatenation

Coordination between High and low level languages

- Future Enhancements

- Conclusion

- References

- Appendices

Abstract

- In this report, the author has put forward the importance of High Performance Computing in

- today’s world. A complete all-round study has been conducted covering the topics of

- parallel programming, GPU computing, memory considerations, programming languages,

- their relative strengths and drawbacks and other topics related to High Performance

- Computing.

- The discussions put forward is neither too high level nor too low level. The concepts of High

- Performance Computing has been put forward with the help of proper examples as well as

- particular implementations in the necessary programming languages and also a thorough

- discussion on the results and the causes for the differences and ways of improvement.

- It is hoped that this study will provide a good insight to programmers interested in the field

- of High Performance Computing about the issues, some techniques and pitfalls which they

- have to look out for. The study will also be helpful to introduce people from a technical

- background with some experience in programming, to the field of High Performance

- Computing.

Introduction

- High Performance Computing abbreviated as HPC, is the art of accumulating and

- aggregating computing power in a manner so as to obtain maximum possible performance

- in order to solve real-life problems in diverse fields like Artificial Intelligence, Big Data

- Analytics, Cloud Computing, Weather Forecasting, Computational Dynamics, Number

- Theory and Cryptography, Bioinformatics and other computational sciences etc. In fact, High

- Performance Computing forms the backbone of almost all the major fields of today’s world.

- This is because nowadays we have an ever-increasing amount of data we have to process in

- order to get desired result, and greater the data and the accuracy, the higher is the

- computational complexity

- and hence the need to use proper techniques to utilise the hardware available for optimal

- performance.

- Importance of HPC in the Job Market

- The field of High Performance Computing is so important that all the tech-giants: Google,

- Microsoft, Amazon, Intel, IBM, Cray, NVIDIA, AMD and many others rely heavily on HPC.

- This is because, for worldwide established companies, they have to design software

- platforms which should be highly scalable and should work without any glitches even under

- extreme workload. For small startups, HPC isn’t of great value because the main motto of

- HPC is to optimise programs for scalability, performance and memory whereas they require

- programs which should work alright without any error. But as they have an increasing

- customer base, HPC concepts gain prime importance. For example, imagine one day the

- Google search engine crashes due to extreme server traffic!!! It’d be an absolute disaster for

- the whole world and the loss in terms of money, data, business considerations is

- unthinkable. Such is the importance of HPC in today’s world.

Languages used in HPC

- In HPC we use mainly bare metal programming languages. In this context, bare metal refers

- to programming languages which do not run on a virtual machine, do not have a garbage

- collector requires almost nothing more than a compiler to generate the machine code

- optimised for the architecture it’ll run on. The primary languages which fall under this

- category are C, C++ and Fortran. These languages are often considered to be “grandfather

- programming languages”. Despite being there for such a long time, they haven’t lost their

- value and are of big importance even in today’s world.

Fortran

- Fortran, the first compiled language, basically gets its name from the term “Formula

- Translate”. It is the first language which made it easier to handle data in the form of arrays,

- matrices and vectors.

- The above feature of array slicing makes it very convenient to handle arrays for a lot of

- computations. And creating such a language in 1957 was a remarkable feat. Moreover

- Fortran remained the fastest language when it came to number crunching for a long time

- until recent times where it has lost its place to modern C++. The reason why Fortran is so

- fast is because Fortran has been there for a long time and the compiler vendors have a lot

- of experience with the Fortran compilers and thus optimise it heavily for numerical

- computations. A prolific example is the automatic vectorization performed by the Fortran

- compilers which greatly reduces the array access time. A single dimensional array (1-D) is a

- block where all the elements are stored in consecutive memory locations. The following

- figure makes it clear:

- Since the elements are stored in consecutive memory locations, the design significantly

- reduces the number of cache misses. Hence, going by the principle of locality of reference,

- when one element is accessed, the nearby memory locations are also loaded in the cache

- and thus the data is consecutively read from the cache memory instead of the main

![Im19](images/Im19)

![Im20](images/Im20)

- memory. Thus iterating over a 1D array is fast and very efficient. But the memory layout of

- multidimensional arrays is in general a bit different:

- The elements of each row are there in consecutive memory locations but multiple rows are

- there in different memory locations. Thus iterating over a multidimensional array is not as

- fast as iterating over a 1D array of the same length. But Fortran compilers are so good at

- optimising that they identify whether the array used in the Fortran code is multidimensional

- or not and vectorizes it. That is, the Fortran compiler vectorizes 1D as well as

- multidimensional arrays assigning consecutive memory locations for the elements. This

- makes array processing so fast in Fortran, and since arrays are the most widely used data

- structures, it makes data processing extremely fast in Fortran.

- Fortran also has a numerous disadvantages. Apart from fast and convenient numerical

- computations, Fortran doesn’t have much to offer. String processing in Fortran is very

- inefficient and is very clumsy as compared to most of the other languages. Also for

- problems requiring a heavy use of complex data structures like sets, maps, priority queues,

- trees and their combinations are quite difficult to program them and much slower

- compared to C++. This gives a big blow to the usage of Fortran. Thus we can see that

- Fortran is not exactly a general-purpose programming language. It was designed specially

- for numerical computations and not as a systems programming language like C or C++.

![Im29](images/Im29)

C

- C is a low-level systems programming language invented by Dennis Ritchie between 1969

- and 1973. Along with C++, it forms the backbone of the IT industry. It is of huge importance

- when designing an Operating System and writing device drivers and kernels. It is also used

- heavily in embedded programming. Coming to the point, C is also used heavily in High

- Performance Computing. The main reason for that is because of the fact that C is a very

- “simple and lightweight” language. It does not have relatively advanced features of high

- level languages like automatic garbage collection by a garbage collector, Object Oriented

- Programming (OOP) features, index checking, good library support as present in high-level

- languages etc. This is one of the reasons why the language is actually very low level. The

- compiler has precise information about the data which is being handled and performs

- aggressive optimizations according to the situation. Moreover unlike Fortran which is used

- primarily for mathematical computations, C can also be used to handle even more complex

- problems with relative ease as compared to Fortran. Because of this C is heavily used in High

- Performance Computing.

- Despite the various pros, C also has a number of problems. C being a low level language,

- makes it very difficult to write proper abstractions for high performant low-level code. That

- is, suppose a library having a lot of features has been designed in C. In order to use it

- effectively in C, the user has to know quite a bit about C programming and more often than

- not is bogged down by the syntax and the various difficulties associated with the language

- like memory management, dangling pointers, data types, poor support for generic

- programming etc rather than focusing more on the problem to be solved. Moreover it can

- be seen that in most cases, if the code written by a novice C programmer is pitted against

- another novice programmer using the high level language, the code of the high level

- language outperforms the C code. This is because it is very easy to write inefficient and error

- prone code in C. In fact, if the program requires quite a bit of dynamic memory

- management, the inexperienced C programmer might write code which can cause

- catastrophic damage to the system because of leaked memory. Writing optimised C code

- requires an in-depth knowledge of C programming making it difficult to program in C.

C++

- C++ is one of the most widely used languages in the industry. Designed by Bjarne Stroustrup

- at AT&T Bell Labs since 1979 C++ is an ideal example of a middle-level, general purpose and

- multi-paradigm programming language with a bias towards systems programming and

- building very efficient, performance-critical long term applications.The only other language

- which is a proper example of a middle-level language present today is Rust, which will be

- discussed later, but Rust being very new is still a lot behind C++ in the number of features.

- Coming to general purpose, C++ can be used to do almost any task one can think of which is

- not possible in high level languages running on a virtual machine and having their own

- garbage collector. For example, we can design an OS in C++, writing lightweight and high

- performance applications which are almost as low as C but then created with a lot less effort

- and is maintainable. Being a middle-level language, C++ has the features of both low level as

- well as high level languages. It is also an ideal example of a multi-paradigm programming

- language. The main features of C++ are:

1. C-style Structural programming

2. Object Oriented Programming (OOP) features like high-level languages, specially

multiple inheritance which is not present in any other language supporting OOPs

paradigm

3. Decent support for functional programming with a relatively high stack-size.

4. Almost zero-cost abstractions most of the time which are determined at compile-

time

5. Direct mapping to hardware because of being very low-level and running on the

system and not on a virtual machine unlike high level languages like Python, Java, C#etc.

6. Has very good support for abstractions and generic programming with the help oftemplates. For example in C++ we can overload operators like +,-,*,/ for specific

types. Thus suppose we have variables x and y which are of matrix types, instead ofwriting x.add(y) or add(x,y) with OOP or functional syntax, we can actually write x+yby overloading the + operator for our matrix type. This is especially helpful while

writing big expressions. In a low level language like C or a high level language like

Java we can’t do this, but in C++ we can do so and at the same time it is almost aslow level as C but also high level as Java, hence being a middle level language.

7. Having support for both manual as well as automatic memory management is a hugefeature. We can manually manage memory with dynamic memory allocation like C.But at times it becomes difficult to manage memory manually. This is where

automatic memory management comes into play and in C++, it is done without agarbage collector. It’s done following a concept known as Resource Acquisition Is

Initialisation (RAII).

8. Template Metaprogramming is another extremely important feature of C++. It is atechnique by which we can make the compiler generate code for us. It is done bytaking advantage of the template instantiation mechanism. It is very crucial for usingspecialised algorithms according to specific cases by not altering a single line of code.This is helpful in optimising programs even more aggressively according to the

context it is used.

9. Speed is also one of the primary features for using C++ in HPC. C++ is one of the

fastest languages present today which are being used widely and was created

keeping in mind the key points of low resource usage, high performance and

expressiveness. Well tuned C++ code runs even faster than well tuned C code in

most occasions.

10. High level language features like the auto keyword for automatic type detection atcompile-time, lambda functions, automatic memory management (mentioned

earlier), full fledged OOP support (mentioned earlier), a completely generic, maturestandard library known as the C++ Standard Template Library (STL) which is tuned foroptimum performance as compared to that of Java where it is not. In fact the

programmers implementing the algorithms and containers of STL, work together

with the compiler designers in order to optimize the STL even according to specificcompilers for optimal performance.

- This plethora of features makes C++ a difficult language for beginners but at the same time

- excellent for serious programmers who want proper control over what they’re doing while

- maintaining a certain high level coding standard.

Importance of C++ in HPC

- The above features make C++ a very good language for high performance computing. In

- fact, the two most important features of C++ is that it maps to hardware directly because of

- being low level and optimise aggressively for the current architecture and the second

- feature is that one can create very good abstractions for C++ code which can be used quite

- easily who are not much into C++. There is no other language in the world which provides

- both of these features simultaneously as good as C++ does. For example C maps to

- hardware directly like C++ but one cannot create proper abstractions with C, and on the

- other hand with a language like Python, we can create very nice and easy to use

- abstractions suitable for beginners but Python being interpreted and running on the virtual

- machine does not map to hardware directly as good as C++. Thus C++ is a language which

- nicely suits the demands of writing highly optimised applications. Another important reason

- for this is due to the fact that C++ has the best optimizing compilers in the world today

- because companies all over the world have invested a lot in order to speed up C++ a lot. The

- following figure shows a list of popular linear algebra libraries available today taken from

- wikipedia:

![Im45](images/Im45)

- The following figure shows a list of popular Deep Learning libraries available today taken

- from Wikipedia:

![Im50](images/Im50)

- Linear Algebra and Deep Learning are important fields which are supported by HPC. And

- both of these fields require performance-critical code and demand very high computing

- power due to large and complex computations. And as evident from the pictures, C++ takes

- the dominant place in HPC as compared to the other languages.

Other languages

- The other popular languages commonly used in High Performance Computing are Python,

- Julia, Haskell. It might be counter-intuitive to use interpreted languages like Python in HPC.

- But then it is seen that the developer’s time is very important as well and Python is a great

- developer-friendly language. In most cases people favour Python over C++ when considering

- the ease of coding, availability of libraries and mainly because of the interactive nature of

- Python. Moreover Python is a much more beginner friendly language than C++. But at the

- same time one has to pay quite a big performance cost while using Python (we’ll be

- discussing more about this in the later sections). In fact it’s so much slow that pure Python is

- considered to be unsuitable for numerical computations for practical applications. Hence

- people have been trying hard to speed up Python. This has been done by letting efficient

- low level languages like C, C++ and Fortran doing all the heavy computations and then

- leaving the lightweight portions for Python. Julia is a language which people can run as fast

- as C at times but maintaining the simplicity of Python. Even Haskell is a language which runs

- C code under the hood and is a strictly functional programming language. But the fact which

- makes Haskell special is that it is tuned specifically for mathematical purposes and the

- compiler, the industrial standard being the Glorious Glasgow Haskell Compiler has incredible

- optimizing capabilities. Optimizing in this case refers to the cases where the compiler often

- improves the algorithmic complexity of the problem which the programmer might fail at

- times. Haskell also has a unique feature of maintaining infinite lists, it automatically goes on

- adding elements indefinitely to the list and as the size grows it goes on removing elements

- from the top of the list. Moreover with features like lazy propagation built-in, Haskell also

- forms a formidable language for HPC. But the serious drawback of Haskell is that the

- programmer is not in proper control of what is going on because the compiler is entrusted

- with a lot of power in Haskell. As a result at times some of the optimizations are actually bad

- and produce slower code. Moreover when well tuned Haskell code is compared against well

- optimized C++ code, it has been seen that the C++ code runs at about 10 times faster on an

- average as compared to the Haskell code.

Important aspects of HPC

Parallel Programming

- Parallel programming forms a fundamental and very important aspect of High Performance

- Computing. In today’s world we no longer use uniprocessor computers. This is the age of

- multiprocessors and clusters. Sequential applications in areas where the task can be made

- parallel are practically of no value because they run on only one core and have no way to

- take advantage of multiple cores. Thus the application which takes some time say t seconds

- to run on an old computer, might take about the same time on a modern multicore

- computer which is of no value as it cannot exploit the available hardware.

- Consider a program of finding the sum of numbers from 1 to N by running a loop adding the

- elements each time. We will be discussing about the effect of parallelism in this example

- and so we will not use the formula n*(n+1)/2. A normal sequential approach will be to run a

- loop from 1 to n and then adding the value of the counter to another global variable already

- initialised to 0 outside the loop. Since this code is sequential it cannot take advantage of

- multiple cores. In order to make this code run in parallel we have to follow a different

- approach. Suppose we have 4 cores and have to find the sum upto 100. We can divide the

- range of 1-100 into 4 ranges i.e. 1-25, 26-50, 51-75 and 76-100. And then we can find the

- sum of these ranges in parallel as the computation of each range is independent of each

- other. Then the 4 sums can be added to the global variable outside the loop. In C++, this

- parallelization of the for loop can be done by adding just one line before the for loop. The

- following figure shows the C++ implementation for the parallel version. The program is quite

- simple and straightforward. We take the input and store it in an integer variable n as shown

- on line number 6. The timer is started at line number 7. The next line has the pragma

- statement which parallelizes the for loop. Removing that statement makes it sequential. We

- then run a for loop from 1 to n and add the elements to the variable sum. We then stop the

- timer and print the time taken for the loop to execute.

![Im61](images/Im61)

- I had compiled this C++ code with GCC 7.2.0 compiler and with optimisations turned on and

- tested it thoroughly on my laptop which has 8GB DDR4 RAM, Intel i7-7700HQ, 2.8-3.8GHz

- clock frequency with a quad core processor and 4 more hyperthreaded cores. The following

- graph shows a proper comparison:

- It has been seen that when run individually with 10^8 as input, the fastest parallel C++ code

- took 0.002 seconds whereas the sequential C++ code took 0.015 seconds to execute. Thus

- the parallel version is about 8X faster than the sequential code which is expected with 8

- cores. It can also be observed that the sequential code is faster than the parallel version for

![Im62](images/Im62)

- small inputs but then as the input grows the parallel code turns out to be faster as seen

- from the graph. This is because spawning a thread pool is quite an expensive task in most

- languages. Typically creation of a new thread takes about 1 MB of RAM. So for small inputs,

- the creation of the thread pool outweighs the loop execution time and thus the sequential

- code runs faster. As the input size grows, the loop iterations take more and more time

- whereas the thread pool creation time and then division of the range into multiple smaller

- ranges remain same. Thus the true effect of parallelism begins to take shape and the parallel

- code dominates. This is an important feature to be kept in mind while designing

- performance-critical applications.

GPU Programming

- Nowadays parallel programming is not only limited to CPUs alone. With the advent of the

- Graphics Processing Unit (GPU), we can write even more massively parallel applications.

- GPUs are optimized to handle an enormous number of computations in parallel. For

- example a mid-range graphics card like the NVIDIA GeForce GTX 1050 installed on my laptop

- has 640 CUDA cores. The following figure makes it clear:

- The GPU cores are optimized for handling parallel computations efficiently. In general the

- CPU handles one thread per core, whereas a GPU can easily handle millions of threads. This

![Im69](images/Im69)

- gives a huge boost in performance. The difference between GPU and CPU can be

- understood from the following figure:

- The arrival of the GPU has thus rocked the world and now we have high-end games which

- look very realistic as compared to the ones from the 1980s.

![Im75](images/Im75)

![Im76](images/Im76)

![Im85](images/Im85)

- The above pictures demonstrate the quality of games running on the CPU before the arrival

- of the GPU. The current games look like:

![Im86](images/Im86)

![Im94](images/Im94)

- The last two pictures have a lot more realistic view of the scene as compared to the

- previous two pictures. This is because of the large number of computations being handled

- by the GPU. As the game progresses, a lot of calculations like the light intensity, the amount

- of detail, the motion of moving objects etc with the matrix and vector calculations are

- performed which are very slow on a CPU. Due to this such good graphics isn’t possible on a

- CPU. Since GPUs so useful, people realised that using them just for graphics alone would be

- a bad idea. So in order to use the power of the GPU for normal computational heavy tasks in

- programs a lot of APIs have been developed. The most popular of them being the NVIDIA

- CUDA API which stands for Compute Unified Device Architecture. But CUDA is available only

- for NVIDIA GPUs. For NVIDIA and other GPUs there is OpenCL. We can call CUDA or OpenCL

- code from normal C, C++ or other languages and thus unleash the power of the GPU. Since

- GPUs supporting these APIs can be used for general purpose tasks as well they’re often

- referred to as GPGPUs which stands for General Purpose Graphics Processing Units.

- In order to show the GPU performance let’s consider a program where we have to sort n

- integers. The parallel C++ implementation of the program followed by the C++ with the

- Thrust API bundled with the NVIDIA Cuda 8.0 Toolkit is shown in the next two figures.

- It is to be noted that the two codes are strikingly similar. The host refers to the CPU and the

- device refers to the GPU. Observing the second code carefully, it can be seen that the input

- integers are stored in a host vector. Then a new device vector is created on the GPU. The

- data from the host vector is copied to the device vector, and then gets sorted in the GPU.

- For further processing, the data in the device vector is copied back to the host vector, but in

- this example we have avoided doing so because we are just measuring the sorting speed.

![Im100](images/Im100)

![Im101](images/Im101)

- The two codes were run with 10^8 random integers and it was found that the CPU C++ code

- takes about 1.81 seconds to sort the integers when compiled with Clang 5.0.0 compiler. On

- the contrary the second code takes about 0.14 seconds to execute. Moreover the second

- code had hardly about 5% GPU utilisation on my machine with 4GB VRAM whereas the first

- code takes about 30% of RAM. Thus the GPU version is about 13X faster than the CPU

- version.

- Despite GPUs being so powerful they have a number of limitations. A GPU is useful only

- when there is a lot of parallel tasks which need to be performed. For sequential tasks, the

- CPU is a lot faster than the GPU. The GPU optimizes for throughput and not latency. And so

- when latency is important, the CPU is always preferred. Moreover the data transfer

- between the CPU and GPU is quite an expensive task. Due to this reason, while writing

- programs, a lot of data is offloaded to the GPU at one go and then the computations are

- performed instead of repeated transfers. If the job requires a lot of repeated data transfers,

- the GPU is probably not a good solution to the problem. Due to these limitations GPUs have

- not been able to replace CPUs. They are used together to solve complex problems.

Memory Considerations

- While solving HPC problems, we often deal with a huge amount of data. In many scenarios

- the data to be processed is too big to be loaded into the RAM. A typical example for such a

- problem would be to process a dataset of size 9GB but my own laptop has a RAM of 8GB.

- Does this mean that the problem cannot be solved? Definitely not! The main solution is to

- read the data in chunks with a predetermined buffer size such that the data loaded in the

- buffer fits into the RAM. In order to illustrate the idea properly let us consider a relatively

- simple problem. Given a text file say of the order of Gigabytes which cannot fit into the

- RAM. We have to copy the text present in the file into a destination file. A sample solution

- would be to read the data in chunks from the source file and write it in the destination file.

- An efficient C++ implementation for the above idea is shown in the next figure. The code

- itself is quite simple and straightforward. Line number 8 removes the synchronization

- between C streams and C++ input-output streams. This line was meant only for speeding up

- the read-write process. At line number 10, a buffer of 1024*1024 characters has been

- declared. Thus at a time at most 2^20 characters are read and stored in the buffer character

- array. The characters are read till the end of file is reached. The code was compiled with

- optimizations and only the reading part was timed with a text file of size 9.9GB on my

- laptop. It was found that the reading took about 76 seconds which is really commendable.

- But even then the readings varied quite a lot because this is quite a heavy task and the

- timings depend a lot on the processes already running on the system.

![Im110](images/Im110)

Interpreted v Compiled languages

- The choice of using a high-level interpreted language or a low-level compiled language has

- always been a topic of heated debates. An interpreted language like Python has the

- advantage of being very readable and many common stuff can be written using less lines of

- code. Moreover being interpreted it is interactive and everything is determined at runtime.

- So the programmer can run portions of code and go on checking the outputs and continue

- programming. In the process if some sections do not give the expected output the

- programmer can always go back, make the necessary changes, run it again till they give the

- required output and continue programming. This style of programming is very helpful and is

- quite fun. Thus the transformation from an idea to the implementation of the problem takes

- very less time when using a language like Python. But then an interpreted has its own set of

- limitations. The code written by the programmer is then read line by line by the interpreted

- and then the necessary actions are carried out. This process is actually very slow as

- compared to compiled languages where the compiler compiles the code written by the

- programmer to efficient machine code and then the entire program is executed. Another

- issue with interpreted languages like Python is that they do have dynamic types, i.e. the

- datatypes of all the variables are determined at runtime. This is infact a double ended sword

- for most programmers. When writing small scale programs say of 100 or even 1000 lines of

- code, its quite easy because the programmer do not have to worry about the datatype of

- the variables. But as the lines of code grows further say about 10000, 1 million etc. then all

- of a sudden the dynamic typing which appeared to be so easy slows the programmer down

- because he needs to keep track of the types of variables being passed and returned from

- various portions of the code. This is because when dealing with such a big codebase, it is not

- possible for the programmer to keep so many things in mind. Whereas compiled languages

- have static types, which means that the data type of any variable is always known at

- compile time. This significantly reduces the burden of the programmer for large programs

- because the types can be determined from the functions and the variable declarations.

- Moreover compiled languages have the ability to generate machine code which is optimised

- for the architecture its running on. Let’s discuss some important points of performance

- difference between Python and C++ in order to get a better understanding of the issues.

Looping speed

- We will revisit the problem of finding the sum of numbers from 1 to N and this time we will

- compare Python implementations against C++. The following graph shows the variation of

- the timings of various implementations:

![Im115](images/Im115)

- We have used CPython 2.7 for our implementation. As seen from the above graph, the

- Python codes for this problem simply don’t stand a chance against their C++ counterparts

- which are barely visible on the graph! The following figure shows the Python

- implementation using for loop:

- The above code snippet is completely readable and doesn’t need any explanation. When

- tested individually, it takes 5.67 seconds to execute for n=10^8 as input. This is 378 times

- slower than the optimized sequential C++ implementation and 2835 times slower than the

- parallel C++ implementation. This is because, since Python is a dynamically typed language,

- the type of the variable cannot be known beforehand and at every iteration, the type of the

- variable i has to be checked and the allocated space has to be resized as and when required.

- Let us consider a different implementation in Python with the help of the built-in sum

- function:

![Im122](images/Im122)

![Im127](images/Im127)

- This Python implementation takes 0.57 seconds to execute. Even though this is about 10X

- faster than the previous implementation, it is still 38 times slower than the sequential and

- 285 times slower than the parallel C++ implementation. This brings us to the following

- conclusions. Iterative tasks are very slow in general for Python. We should avoid loops as

- much as we can. The built-in sum function runs a loop internally written in C because the

- CPython interpreter itself is written in C. But then as evident from the results, a bare metal

- C++ (or even C in this case) is much faster than a Python implementation. And since loops

- are very important loop constructs, we should be very careful in such scenarios and should

- try to vectorize our code as much as possible.

String Concatenation

- Strings are yet another important data type which is used heavily when handling textual

- data and especially in fields like Natural Language Processing (NLP). So string concatenation

- is a very vital operation in such areas. Let us consider a program where we have to take an

- integer N as input and then concatenate all the numbers from 1 to N into a single string. For

- example, if the user gives 6 as input, the program should form a string “123456” by

- concatenation of all the numbers from 1 to N. Let us consider two Python implementations

- for the problem.

![Im131](images/Im131)

- The two implementations are quite readable but has a subtle difference. In the first

- implementation we are creating an array of integers from 1 to N and then converting the

- entire array to a string. In the second implementation we are concatenating all integers with

- a blank string in the beginning using the join function. Let us now look at two C++

- implementations

- for the problem.

![Im132](images/Im132)

![Im138](images/Im138)

![Im139](images/Im139)

- The above two implementations are also readable. In the first implementation we are

- running a loop from 1 to N and then the value of the loop counter i is being changed to a

- string and then concatenated with the string variable str. The second example is slightly

- different where instead of concatenating with a string we are using a stringstream variable

- which is present in the C++ STL. The two operations are essentially the same but a stream is

- used in the second case. The following graph of the timings makes it clear.

![Im145](images/Im145)

- It can be seen that the stringstream implementation with C++ turns out to be the fastest.

- Followed by the Python implementation with the array module. Then comes the string

- implementation in C++ and at last the join function in Python. As we can see that in this

- example Python is quite close to C++. The stringstream class in C++ is much more efficient

- than the string class, and this is an important point which should be kept in mind while

- handling strings with C++. In Python we should avoid using the join function, and despite

- being quite inefficient it is used freely by people. Converting an array to a string is much

- more efficient. Another thing to be noted is that we should avoid running a loop from 1 to N

- in Python at all costs unlike the C++. Had it been so, the Python timings would have

- skyrocketed. And the C++ timings would have been barely visible.

Coordination between High and low level languages

- As evident from the above results, low level languages like C++ are ideal for performance

- critical applications. Moreover the string concatenation program written in modern C++ (C+

- +11 and beyond) is quite compact and readable. An equivalent efficient C implementation

- would have been very difficult to write. Thus C++ offers very high speed and also a good

- degree of readability. But then high level languages like Python are truly very easy to write

- and much more suitable for beginners. So the best possible thing which can be done is

- combining Python and C++ code in a single program so that the Python code calls a

- precompiled code written in a low-level language like C, C++ or Fortran and thus have the

- readability of Python and also the performance of a bare-metal language. People all over

- the world have put a lot of effort in doing this. We now have APIs like SWIG (Simplified

- Wrapper and Interface Generator), PyBind11, Boost.Python, Cython etc. These tools help us

- to combine C and C++ code with Python. Thus the main heavy lifting is done by the bare

- metal language and then a Python wrapper is created so that Python can call that code.

- Numba is a JIT (Just In Time) compiler for Python, which compiles the Python code on the fly

- to C. We also have PyCUDA for using CUDA from Python. These features are being used

- heavily by people all over the world. The Linear Algebra and the Deep Learning libraries

- which were listed before, most of them had a Python interface which made it easy to use

- such libraries from Python. Numpy is a very efficient numerical computation library for

- Python which has been written in C and has Python wrappers created with Cython. Initially it

- used SWIG for the purpose. Numpy provides very efficient N-dimensional arrays for Python

- in addition to linear algebra functions from BLAS (Basic Linear Algebra Subprograms),

- LAPACK (Linear Algebra Package) which are written in C, C++ and Fortran. There are also

- libraries like SciPy which are written in C then wrapped for Python. All these tools combined

- with the interactive nature of Python makes it a very good language for HPC in general.

Future Enhancements

- Going by the current trends, the CPU clock speeds are reaching their limits and we aren’t

- getting modern processors with significantly higher clock speed. And therefore the current

- trend is to increase the level of parallelism and club as many processors possible into a

- single chip. Due to this reason the importance of parallel programming and programming

- with clusters are increasing rapidly. Talking about parallel programming, the hot topic is

- GPU programming, and the best part is that even though CPU speeds are becoming

- stagnant, GPU performance is still growing rapidly as shown in the figure:

- This is the primary reason that GPUs are dominating the fields of computing. The term GPUs

- along with Deep Learning go hand-in-hand and we simply cannot imagine playing a high-end

- game without a GPU today. Moreover the 21st century being the era of Artificial

- Intelligence, GPUs are playing a prime role. Hence people are shifting their focus gradually

- from CPU parallelism to GPU parallelism and improving the bottlenecks of GPU

- programming. The current trend is to offload code and data as efficiently as possible to the

- GPU and retrieving the processed data efficiently. This is so widespread that the ISO C++

- Committee are considering the decision of whether to make GPU programming a part of the

- standard C++, so that C++ programmers do not have to rely on third party APIs for GPU

- programming. This would give a big boost to the power of C++ and would also make GPU

- programming quite simpler.

Conclusion

- The field of High Performance Computing is of great value today and in the generations to

- come. This is a field which will never stop growing because no matter what happens, we can

- safely assume that computers won’t have infinite clock speed or infinite memory available

- to them. Had it been so, the field of High Performance Computing would not have existed.

- We would only have to worry about solving the problem and focused on writing short,

- elegant and readable code and being least bothered about performance. But unfortunately

- (or fortunately!!!) this is not the case and as long as the speed and memory of a computer

- has its limits, mankind will always try to push them further and further and this is exactly

- where High Performance Computing will always come in handy. Thus being absolutely

![Im155](images/Im155)

- entangled with mankind’s need for speed, High Performance Computing is one of the very

- few fields which will never lose its importance.

References

1. This is the link to my Github repository.

This repository is being maintained by meand Soumyojit Chatterjee where we are analysing the performance differences

between Python and C++. The codes being put forward in this report have been

taken from our repository. The C++ programs are coded by me and the Python

programs are coded by Soumyojit.

a. This is the link to the summation problem

as discussed in this report. The

codes for the summation problem and the graphs have been taken from thisfolder.

have been taken from this folder.

problem. The codes and graphsb. This is the link to the string concatenation

2. This is the link to the NVIDIA official website.

3. This is the link to my detailed system specs

conducted.

on which the benchmarks have been

Appendices

1. This is the link to my Github profile.

2. This is the link to the NVIDIA developer site.

Anyone with a thirst for C++ will find my profileuseful. It contains quite a few utility tools I have developed myself for C++

programming.

GPU programming with CUDA here.

for Intel CPUs, in fact, for Intel CPUs it is one of the fastest in the world right now.it very simple to combine Python and C++ code.

One can find vital information about

It is a highly optimised Math libraryAs discussed earlier, Pybind11 makes4. This is a link to the pybind11 github repository.

3. This is the link to the Intel Math Kernel Library.

