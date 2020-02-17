Date 21/02/2019 , mauro r
Unsigned comparison bug!Comparison is downgraded to unsigned int , the workaround is to cast the the macro to  ( d  <  (int) ARRAY_TOTAL_ELEMENTS)

#include  <stdio.h>int array[] = {23, 34 ,12 ,17 ,204 , 99, 16};
#define ARRAY_TOTAL_ELEMENTS (sizeof(array)/ sizeof(array[0]))
int main(void){

int d = -1;

printf("Comparing [%d < %lu]\n",d,  ARRAY_TOTAL_ELEMENTS);


if (d < ARRAY_TOTAL_ELEMENTS)


printf("Signed comparisson asserted [%d is less than %lu]", d, ARRAY_TOTAL_ELEMENTS);


else


printf("Unsigned comparisson asserted [%d is greater than %lu]", d, ARRAY_TOTAL_ELEMENTS);

		return 0;

}

Another Example,

#include  <stdio.h>

#include <stdint.h>
#define FOO 0xFFFFint main(void){
int16_t bar = FOO;

if (FOO == bar )

printf("expected result %d  == %d\r\n" , FOO , bar);


else

printf("no so expected result %d != %d \r\n" , FOO, bar);

	   return 0;

}



Variable initialization (stack frame) For non static variables, always initialize your variable, otherwise it would be initialized with garbage. the output of the code below is



#include  <stdio.h>void foo(void){
int a;

printf("a: %d \n",a);


}void bar(void){
int a = 66;
	}int main(void){

bar();

	foo();


return 0;
}

OUTPUT :  a: 66

Always match the qualifier or in this case Const shall be interpreted as ReadOnly !  A const qualifier doesn't make the variable constant, it does only tells the compiler  and programmer that is a read only variable since it value can be changed :



#include  <stdio.h>
int main(void)
{
const char foo = 'A';

char * foo_ptr  = &foo;



printf("Foo is constant ?   foo = %c \n",foo);


*foo_ptr = 'B';

		printf("Well,it did change, foo = %c \n",foo);



return 0;

}
OUTPUT :  Foo is constant ?   foo = AWell,it did change, foo = Bhowever this can be prevented from happening through the foo_ptr itself if we match the qualifier for the pointer:const char * foo_ptr  = &foo;

in this manner the compiler would rice the error , but we still
can copy the const pointer to another pointer and do the same;
 To summarize const  doesn't really meaning a constant value in C.Error(s):source_file.c: In function ‘main’:source_file.c:10:14: error: assignment of read-only location ‘*foo_ptr’
  *foo_ptr = 'B';



   ^STRING LIST  !  The bug in the following snippet bug consist of  a missing comma in the string list,
the compiler will  joint strings without rissing any messages:

/*NO BUG: all comma are present*/
char * available_sensors[ ] = { "Asensor" ,
"Bsensor" ,
"Csensor" ,
"Dsensor"
};

  OUTPUT:
Asensor
Bsensor
Csensor
Dsensor

/*BUG: missing a comma !!*/
char * available_sensors[ ] = {
"Asensor" ,
"Bsensor"
"Csensor" ,
"Dsensor"
};

OUTPUT:
Asensor
Bsensor
Csensor
Dsensor

WHY sizeof  foo won't work in file2.c?file1.c:extern int foo[];

file2.c:int foo[] = {1, 2, 3};

* the extern declaration of an Array  with an unspecified size is an incomplete type;

* sizeof operates at compile time

/* END OF THE NOTE */
