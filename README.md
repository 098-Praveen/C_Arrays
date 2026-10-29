# C_Arrays

STAGE 1:
WHY ARRAYS:
IF I WANT YOU TO STORE 5 ELEMENTS IT IS FINE LIKE
int a=10;
int b=20;
int c=40;
int d=50;
int e=60;
WHAT IF I ASKED YOU TO STORED 100 VARIABLES:

THAT WOULD BE INCOVENIENT RIGHT:
THAT IS WHY WE USE ARRAYS 
C PROVIDES A WAY TO STORE MULTIPLE ELEMENTS OF THE SAME DATA TYPE UNDER ONE VARIABLE
NAME:
THIS IS CALLED ARRAY:

INT ARR[5]={10,20,30,40,50};
INT IS DATA TYPE
ARR IS NAME OF THE ARRAY
[5] IS ARRAY SIZE 
10,20,30,40,50 ARE INITIAL VALUES:

TO ACCESS THE PARTICULAR INDEX WE USE ARRAY INDEX
QUESTION:
int arr[5] = {10, 20, 30, 40, 50};
how many integers can this array hold?
5
we have 5 elements but how to access these 5 elements
for that we use array index 

STAGE 2: ARRAY INDEX:

array index always starts from 0 to size-1 
so like 0->5-1 so 0--->4.
a[0]=10
a[1]=20;
a[2]=30;
a[3]=40;
a[4]=50;
to print we use printf("%d",a[0]) we use index values which value we want to print

QUESTION:
int arr[5] = {10, 20, 30, 40, 50};
if i suppose printf("%d",arr[5]);
ANS: IT ACCESS AN ELEMENT OUTSIDE THE ARRAY'S VALID BOUNDS, CAUSING UNDEFINED BEHAVIOR.

STAGE 3: ARRAY DECLARATION AND INITIALIZATION:
DECLARATION: 
int arr[5];
HERE WE NEED TO ASSIGN VALUES TO INDEX;

DECLARATION WITH INITIALIZATION:
int arr[5]={10,20,30,40,50};

AND LETTING THE COMPILER DECIDE THE SIZE OF THE ARRAY:
int arr[]={10,20,30};
HERE THE COMPILER DETERMINES THE SIZE OF THE ARRAY BY SEEING THE INITIALIZERS:
NOW THE QUESTIONS:

int arr[5] = {10, 20};
what stores after the 1 to 4
COMPILER INITIALIZES THEM TO 0
WHEN AN ARRAY IS INITIALIZED WITH FEWER VALUES THAN IT'S DECLARED SIZE, ALL REMAINING ELEMENTS ARE INITIALIZED TO 0

STAGE 4: ACCESSING ARRAY ELEMENTS USING LOOPS:
int arr[5]={10,20,30,40,50};
here if you want to print
printf("%d ",a[0]);
printf("%d ",a[1]);
printf("%d ",arr[2]);
printf("%d ",arr[3]);
printf("%d ",arr[4]);

what if you need to print 100 elements that would be inconvenient

so for that here we use loops:
for(int i=0;i<5;i++)
{
printf("%d ",arr[i]);
}
  QUESTIONS
  int arr[5] = {2, 4, 6, 8, 10};

for (int i = 1; i < 4; i++)
{
    printf("%d ", arr[i]);
}
ANS IS 4,6,8
3 TIMES 

STAGE 5:
FINDING THE SUM OF ARRAY ELEMENTS:
#include<stdio.h>
int main()
{
    int arr[5]={10,20,30,40,50};
    int sum=0,i;
    for(i=4;i>=0;i--)
    {
        sum=sum+arr[i];
    }
    printf("%d ",sum);
}
FINDING AVERAGE:
FORMULA: 
AVERAGE=SUM OF ALL ELEMENTS/NUMBER OF ELEMENTS
#include<stdio.h>
int main()
{
    int arr[5]={2,4,6,8,10};
    int sum=0,i,average;
    for(i=4;i>=0;i--)
    {
        sum=sum+arr[i];
    }
    printf("%d ",sum);
    average=sum/5;
    printf("%d",average);
}

FINDING THE LARGEST ELEMENT IN AN ARRAY:

#include<stdio.h>
int main()
{
    int arr[5]={2,4,10,8,6};
    int large=arr[0];
    for(int i=0;i<5;i++)
    {
        if(arr[i]>large)
        {
            large=arr[i];
        }
    }
    printf("large:%d ",large);
}

FINDING THE SMALLEST ELEMENT IN AN ARRAY
#include<stdio.h>
int main()
{
    int arr[5]={10,4,2,8,6};
    int small=arr[0];
    for(int i=0;i<5;i++)
    {
        if(arr[i]<small)
        {
            small=arr[i];
        }
    }
    printf("small:%d ",small);
}

SEARCHING FOR AN ELEMENT:

#include<stdio.h>
int main()
{
    int arr[5]={10,4,2,8,6};
    int found=2;
    for(int i=0;i<5;i++)
    {
        if(arr[i]==found)
        {
            printf("found");
        }
    }
    
}

#include<stdio.h>
int main()
{
    int arr[5]={10,20,30,40,50};
    int found=40;
    for(int i=0;i<5;i++)
    {
        if(arr[i]==found)
        {
            found=1;
        }
    };
    if(found==1)
        printf("number is found");
    else
        printf("number is not found");
    
}

FINDING EVEN AND ODD ELEMENTS IN AN ARRAY:
#include<stdio.h>
int main()
{
    int arr[5]={10,20,30,43,50};
    int even=0,odd=0;
    for(int i=0;i<5;i++)
    {
        if(arr[i]%2==0)
        {
            even++;
        }
        else
        {
            odd++;
        }
    }
    printf("%d ",even);
    printf("%d ",odd);
}
PROBLEM: 
STAGE 10: COUNTING POSITIVE, NEGATIVE, AND ZERO ELEMENTS:
#include<stdio.h>
int main()
{
    int arr[7]={-5,10,0,-2,8,0,3};
    int positive=0,negative=0,zeroes=0;
    for(int i=0;i<7;i++)
    {
        if(arr[i]>0)
        {
            positive++;
        }
        else if(arr[i]<0)
        {
            negative++;
        }
        else
        {
            zeroes++;
        }
    }
    printf("positive:%d negative:%d zeroes:%d",positive,negative,zeroes);
    return 0;
    
}

STAGE 11: REVERSING AN ARRAY:
ARRAY IS arr[5]={10,20,30,40,50};

#include<stdio.h>
int main()
{
    int a[5]={10,20,30,40,50};
    int i,j,temp;
    for(i=0,j=4;i<j;i++,j--)
    {
        temp=a[i];
        a[i]=a[j];
        a[j]=temp;
    }
    for(i=0;i<5;i++)
    {
        printf("%d ",a[i]);
    }
    return 0;
}

SORTING TECHNIQUES:
PLS DO REVISION:






