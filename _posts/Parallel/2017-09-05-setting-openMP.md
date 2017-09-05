---
layout: post
title:  "OpenMP start"
date:   2017-09-05
categories: Parallel
comments: false
---

* content
{:toc}

### Class
* Name : Parallel Scientific Computing (2017 Fall)
* Contents : OpenMP and MPI programming

### OpenMP setting in Visual Studio
* Reference site :  [http://untitledtblog.tistory.com/33](http://untitledtblog.tistory.com/33)

### Simple Hello example
* Code :   
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

* Result :   
![hello_result](HanulK.github.io/_posts/Parallel/hello.PNG)
