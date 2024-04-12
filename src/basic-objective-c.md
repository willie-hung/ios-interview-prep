## Objective-C Basics

> Objective-C is general-purpose language that is developed on top of C Programming language by adding features of Small Talk programming language making it an object-oriented language.

#### 1. Functions

```objective-c
#import <Foundation/Foundation.h>

@interface SampleClass:NSObject
/* method declaration */
- (int)max:(int)num1 andNum2:(int)num2;
@end

@implementation SampleClass
/* method returning the max between two numbers */
- (int)max:(int)num1 andNum2:(int)num2 {

   /* local variable declaration */
   int result;

   if (num1 > num2) {
      result = num1;
   } else {
      result = num2;
   }

   return result;
}
@end

int main(int argc, const char * argv[]) {
    /* local variable definition */
   int a = 100;
   int b = 200;
   int ret;

   SampleClass *sampleClass = [[SampleClass alloc]init];

   /* calling a method to get max value */
   ret = [sampleClass max:a andNum2:b];

   NSLog(@"Max value is : %d\n", ret );
   return 0;
}
```

[Source](https://www.tutorialspoint.com/objective_c/objective_c_functions.htm)

#### 2. Blocks

> Distinct segments of code that can be passed around to methods or functions as if they were values.

```objective-c
#import <Foundation/Foundation.h>

typedef void (^CompletionBlock)(void);
@interface SampleClass:NSObject
- (void)performActionWithCompletion:(CompletionBlock)completionBlock;
@end

@implementation SampleClass

- (void)performActionWithCompletion:(CompletionBlock)completionBlock {

   NSLog(@"Action Performed");
   completionBlock();
}

@end

int main(void) {

   /* my first program in Objective-C */
   SampleClass *sampleClass = [[SampleClass alloc]init];
   [sampleClass performActionWithCompletion:^{
      NSLog(@"Completion is called to intimate action is performed.");
   }];

   return 0;
}
```

[Source](https://www.tutorialspoint.com/objective_c/objective_c_blocks.htm)

#### 3. Array

```objective-c
#import <Foundation/Foundation.h>

int main (void) {
   int n[10];   /* n is an array of 10 integers */
   int i, j;

   /* initialize elements of array n to 0 */
   for (i = 0; i < 10; i++) {
      n[i] = i + 100;    /* set element at location i to i + 100 */
   }

   /* output each array element's value */
   for (j = 0; j < 10; j++) {
      NSLog(@"Element[%d] = %d\n", j, n[j]);
   }

   return 0;
}
```

[Source](https://www.tutorialspoint.com/objective_c/objective_c_arrays.htm)

#### 4. Pointers

```objective-c
#import <Foundation/Foundation.h>

int main (void) {
   int  var = 20;    /* actual variable declaration */
   int  *ip;         /* pointer variable declaration */
   ip = &var;       /* store address of var in pointer variable*/

   NSLog(@"Address of var variable: %p\n", &var  );

   /* address stored in pointer variable */
   NSLog(@"Address stored in ip variable: %p\n", ip );

   /* access the value using the pointer */
   NSLog(@"Value of *ip variable: %d\n", *ip );

   return 0;
}
```

```
Output:
Address of var variable: 6fdff168
Address stored in ip variable: 6fdff168
Value of *ip variable: 20
Program ended with exit code: 0
```

[Source](https://www.tutorialspoint.com/objective_c/objective_c_pointers.htm)
