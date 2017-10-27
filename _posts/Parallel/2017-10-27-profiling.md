---
layout: post
title:  "What's the profiling"
date:   2017-10-27
categories: Parallel
comments: false
---

* content
{:toc}

### What is profiling?
* Allows you to learn
- where your program is spending its time
- what functions called what other functions
* Can show you which pieces of your program are slover than you expected
- might be candidates for rewriting
* Show which functions are being called more or less often than expected

### Profilers
* Use information collected during the actual execution of a program
* Available Profilers
- Gprof
- Intel VTune
- PGI pgprof
- others ...

#### Gprof
It is the GNU project Profilers.

* Profiler steps
- compile and link your program with profiling enabled
- excute your program to generate a profile data file
- run profiler to analyze the profile data

* Call graph
It shows, for each function
:
:
:

```
  #include <stdio.h>   
  #include <omp.h>   

  int main()   
  {   
    #pragma omp parallel   
	   {   
		     printf("Hello, Start openMP \n");   
	   }   

	   return 0;   
  }   
```
