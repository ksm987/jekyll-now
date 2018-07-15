---
layout: post
title: Lv.1 Multiples of 3 and 5
---

출처: [http://codingdojang.com/scode/350#answer-filter-area](http://codingdojang.com/scode/350#answer-filter-area)

[문제] 

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23. 

Find the sum of all the multiples of 3 or 5 below 1000. 



[번역] 

10미만의 자연수에서 3과 5의 배수를 구하면 3,5,6,9이다. 이들의 총합은 23이다. 

1000미만의 자연수에서 3,5의 배수의 총합을 구하라.

----

### [java]
```java
public class Test { 
        public static void main(String[] args) { 
               Multiple_of_3and5(1000); 
    } 

        public static void Multiple_of_3and5(int num) { 
               int result=0; 

               for(int i=1; i<num; i++) { 
                       if(i % 3 == 0 || i % 5 == 0) { 
                              result+=i; 
                       } 
               } 
               System.out.println("3,5의 배수의 총합: " + result ); 
        } 

}
```
----

### [python]
```python
def Multiple_of_3and5(num):
     result=0
     for i in range(1,num):
         if i%3==0 or i%5==0:
             result+=i
     print("3,5의 배수의 총합: " ,result)
 
 Multiple_of_3and5(1000)
```
----

### [c]
```c
#include <stdio.h>
void Multiple_of_3and5(int num);

int main()
{
   Multiple_of_3and5(1000);
   return 0;
}

void Multiple_of_3and5(int num)
{
   int result = 0;
   for (int i = 0; i < num; i++) {
      if (i % 3 == 0 || i % 5 == 0) {
         result += i;
      }
   }
   printf("3,5의 배수의 총합 : %d\n", result);
}
```
----

[출력]
3,5의 배수의 총합 : 233168
