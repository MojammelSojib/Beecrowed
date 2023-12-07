check prime number
#include<stdio.h>
int main()
{
    int n,count=0,totalprime=0,sum=0;

    for(n=1;n<=10000;n++){
            count=0;
    if(n<=1){
            count=1;
        }
        else{
        for(int i=2;i<n;i++){
            if(n%i==0){
                count++;
                break;
            }
         }
        }
        if(count==0)
        {
            printf("%d \n",n);
    totalprime++;
    sum=sum+n;
         }
        }
        printf("Total Prime Numbers:%d \n",totalprime);
        printf("Total Sum Prime Numbers:%d ",sum);
        return 0;

}
check factorial number code

#include<stdio.h>
int main()
{
  int i,fact=1,n;
  printf("Enter any positive number:");
  scanf("%d",&n);

  for(i=1;i<=n;i++)
  {
      fact =fact*i;
  }
  printf("%d\n",fact);
  return 0;
}

**sum of digits**
#include<stdio.h>
int main()
{
    int num,tem,r,sum=0;
    printf("Enter any number ");
    scanf("%d",&num);

    tem=num;
    while(tem!=0)
    {
        r=tem%10;
        sum=sum+r;
        tem=tem/10;
    }
    printf("%d",sum);

}

**revers of number**

#include<stdio.h>
int main()
{
    int n,tem,r,sum=0;
    printf("Enter your number ");
    scanf("%d",&n);

    tem=n;

      while (tem!=0) {
        r = tem % 10;
        sum = sum * 10 + r;
        tem = tem / 10;
    }
  printf("Revers of number %d",sum);
    return 0;
}


**Palindrome number**


#include<stdio.h>
int main()
{
    int n,tem,r,sum=0;
    //printf("Enter any number ");
    scanf("%d",&n);

    tem=n;
    while(n!=0)
    {
        r=tem%10;
        n=sum*10+r;
        tem=tem/10;
    }
    if(n==sum){
        printf("Palindrome");
        }
    else{
        printf("Not");
       } 
        return 0;

}
**Armstrong Number**
#include<stdio.h>

int main() {
    int n, tem, r, sum = 0;
    printf("Enter any number: ");
    scanf("%d", &n);

    tem = n;
    while (tem != 0) {
        r = tem % 10;
        sum = sum + r * r * r;
        tem = tem / 10;
    }

    if (sum == n) {
        printf("Armstrong Number");
    } else {
        printf("Not Armstrong Number");
    }

    return 0;
}

**Counting number of a digit in an integer**
#include<stdio.h>
int main()
{
    int n,count=0;

    printf("Enter Your digit : ");
    scanf("%d",&n);

    while(n!=0)
    {
        n=n/10;
        count++;
    }
    printf("Total number of digit:%d\n",count);
    return 0;
}

**Strong Number**
#include<stdio.h>
int main()
{
    int n,sum=0,r,tem,i,fact;

    printf("Enter a integer: ");
    scanf("%d",&n);

    tem=n;
    while(tem!=0)
    {
        r=tem%10;
        fact=1;
        for(i=1;i<=r;i++)
        {
            fact=fact*i;
        }

        sum=sum+fact;
        tem=tem/10;
    }
    if(sum==n){
        printf("%d is Strong number ",n);
    }else
    {
         printf("%d is not Strong number ",n);
    }
    return 0;
}
**  Series – 1**
#include<stdio.h>
int main()
{
    int n,i,sum=0;
    printf("Enter the last digit: ");
    scanf("%d",&n);
    printf("1+3+5+.....+%d",n);

    for(i=1;i<=n;i=i+2)
    {
        sum=sum+i;
    }
    printf("=%d\n",sum);
    return 0;
}
**  Series – 2**
#include<stdio.h>
int main()
{
    int n,a=1,sum=0;
    printf("Enter the last digit: ");
    scanf("%d",&n);
    printf("1+2+3+.....+%d",n);

   while(a<=n)
    {
        sum=sum+a;
        a=a+1;
    }
    printf("=%d\n",sum);
    return 0;
}
**SUM of Even Number**
#include<stdio.h>
int main()
{
    int i,n,sum=0;
    printf("Entre your Number: ");
    scanf("%d",&n);

    for(i=2;i<=n;i=i+2)
    {

       printf("%d ",i);
       sum=sum+i;
    }
    printf("\nSum = %d\n",sum);
    return 0;

}
**Maximum and Minimum of Array**
#include<stdio.h>

int main() {
    int num[1000], n, i;

    printf("How many Numbers: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        scanf("%d", &num[i]);
    }

    int max = num[0];
    int maxIndex = 0;

    for(i = 1; i < n; i++) {
        if (max < num[i]) {
            max = num[i];
            maxIndex = i;
        }
    }
    
    printf("Maximum variable = %d\n", max);
    printf("Position (index) of maximum variable = %d\n", maxIndex+1);

    return 0;
}

    Fibonacci series 

#include<stdio.h>

int main() {
    int a[100], n, i;

    printf("How many Numbers: ");
    scanf("%d", &n);

    a[0]=0;
    a[1]=1;

    for(i = 2; i < n; i++)
    {
        a[i]=a[i-1]+a[i-2];
    }
    printf("\n");
      for(i = 0; i < n; i++)
      {
          printf("%d ",a[i]);
      }

      return 0;
}

Array | Searching a number (Linear search)
#include<stdio.h>
int main()
{
    int num[9]={10,5,17,18,90};
    int value,pos=-1,i;
    printf("Enter the value you want to search: ");
    scanf("%d",&value);

    for(i=0;i<9;i++)
        {
            if(value==num[i])
            {
                pos=i+1;
                break;
            }
        }

    if(pos==-1)
    {
        printf("Not Found");
    }
    else
    {
        printf("The poistion %d",pos);
    }
    return 0;
}
copy all elements of an array to another array

#include<stdio.h>

int main() {
    int array1[50], array2[50], i, n;

    printf("How many numbers: ");
    scanf("%d", &n);

    // Input elements for array1
    printf("Array1: ");
    for (i = 0; i < n; i++) {
        scanf("%d", &array1[i]);
    }

    // Display elements of array1
    printf("Array1: ");
    for (i = 0; i < n; i++) {
        printf("%d ", array1[i]);
    }

    // Copy elements from array1 to array2
    for (i = 0; i < n; i++) {
        array2[i] = array1[i];
    }

    // Display elements of array2
    printf("\nArray2: ");
    for (i = 0; i < n; i++) {
        printf("%d ", array2[i]);
    }

    return 0;
}

2D Array

#include<stdio.h>

int main() {
    int i, j;
    int A[3][4];

    // Input
    for(i = 0; i < 3; i++) {
        for(j = 0; j < 4; j++) {
            scanf("%d", &A[i][j]); // Add & before A[i][j]
        }
    }

    // Output
    for(i = 0; i < 3; i++) {
        for(j = 0; j < 4; j++) {
            printf("%d ", A[i][j]); // Print a space after each element
        }
        printf("\n"); // Add a newline after each row
    }

    return 0;
}
