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
Simple Matrix
#include<stdio.h>

int main() {
    int i, j;
    int A[3][4],B[3][4];

    // Input A
    printf("Enter elements For A Matrix. ");
    for(i = 0; i < 3; i++)
    {
        for(j = 0; j < 4; j++)
        {
            printf("A[%d][%d]= ",i,j);
            scanf("%d", &A[i][j]); // Add & before A[i][j]
        }
        printf("\n");
    }

    printf("A= ");
    // Output for A matrix
    for(i = 0; i < 3; i++)
    {
        printf("\t");
        for(j = 0; j < 4; j++) {
            printf("%d ", A[i][j]); // Print a space after each element
        }
        printf("\n"); // Add a newline after each row
    }


    // Input B
    printf("Enter elements For b Matrix.");
    for(i = 0; i < 3; i++)
    {
        for(j = 0; j < 4; j++)
        {
            printf("B[%d][%d]= ",i,j);
            scanf("%d", &B[i][j]); // Add & before A[i][j]
        }
        printf("\n");
    }

    printf("B=");
    // Output for A matrix
    for(i = 0; i < 3; i++)
    {
        printf("\t");
        for(j = 0; j < 4; j++) {
            printf("%d ", B[i][j]); // Print a space after each element
        }
        printf("\n"); // Add a newline after each row
    }

    return 0;
}
#include<stdio.h>

int main() {
    int i, j,row,colum;
    int A[10][10],B[10][10],C[10][10];

    printf("Enter the number row and colum: ");
    scanf("%d %d",&row,&colum);

    // Input A
    printf("Enter elements For A Matrix. \n");
    for(i = 0; i < row; i++)
    {
        for(j = 0; j < colum; j++)
        {
            printf("A[%d][%d]=",i,j);
            scanf("%d", &A[i][j]); // Add & before A[i][j]
        }
        printf("\n");
    }

     printf("Enter elements For B Matrix. \n");
    for(i = 0; i < row; i++)
    {
        for(j = 0; j <colum; j++)
        {
            printf("B[%d][%d]= ",i,j);
            scanf("%d", &B[i][j]); // Add & before A[i][j]
        }
        printf("\n");
    }

    printf("A= ");
    // Output for A matrix
    for(i = 0; i < row; i++)
    {
        printf("\t");
        for(j = 0; j < colum; j++) {
            printf("%d ",A[i][j]); // Print a space after each element
        }
        printf("\n"); // Add a newline after each row
    }


    // Input B


    printf("\nB=");
    // Output for A matrix
    for(i = 0; i < row; i++)
    {
        printf("\t");
        for(j = 0; j < colum; j++) {
            printf("%d ", B[i][j]); // Print a space after each element
        }
        printf("\n"); // Add a newline after each row
    }

    //addition

    for(i = 0; i < row; i++)
    {
        for(j = 0; j < colum; j++)
        {
           C[i][j]=A[i][j]+B[i][j];
        }

    }

    printf("\nA + B = ");
    for(i = 0; i < row; i++)
    {

        for(j = 0; j < colum; j++)
        {
           printf("%d ",C[i][j]);
        }

        printf("\n");
        printf("\t");
    }

    return 0;
}

 Matrix Multiplication

 #include<stdio.h>
int main()
{
    int first[10][10],sec[10][10],result[10][10],sum=0,r1,r2,c1,c2,i,j,k;
    //int i;
    printf("Enter row and col for first matrix: ");
    scanf("%d %d",&r1,&c1);

    printf("Enter row and col for second matrix: ");
    scanf("%d %d",&r2,&c2);

    while(c1!=r2)
    {
        printf("Error !! colum of first matrix not equal to row of second matrix");
            printf("Enter row and col for first matrix: ");
    scanf("%d %d",&r1,&c1);

    printf("Enter row and col for second matrix: ");
    scanf("%d %d",&r2,&c2);
    }
    //taking input for first matrix

    printf("\nEnter elements for first matrix\n");
    for(int i=0;i<r1;i++)
    {
        for(j=0;j<c1;j++)
        {
            printf("First [%d] [%d] = ",i,j);
            scanf("%d",&first[i][j]);
        }

    }


    //2nd input

    printf("\nEnter elements for 2nd matrix\n");
    for(int i=0;i<r2;i++)
    {
        for(j=0;j<c2;j++)
        {
            printf("First [%d] [%d] = ",i,j);
            scanf("%d",&sec[i][j]);
        }

    }
    //multiplication

    for(i=0;i<r1;i++)
    {
        for(j=0;j<c2;j++)
        {
            for(k=0;k<c1;k++)
            {
                sum=sum+first[i][k]*sec[k][j];
            }
            result[i][j]=sum;
            sum=0;
        }
    }


    //printing 1st matrix
    printf("\n\nFirts Matrix \n");
        for(i=0;i<r1;i++)
    {

        for(j=0;j<c1;j++)
            printf("%d ",first[i][j]);
            printf("\n");
    }

    //out 2nd

     printf("\n\n2nd Matrix \n");
        for(i=0;i<r2;i++)
    {

        for(j=0;j<c2;j++)
            printf("%d ",sec[i][j]);
            printf("\n");
    }

    //printing result matrix
        //out 2nd

     printf("\n\nResult Matrix \n");
        for(i=0;i<r1;i++)
    {

        for(j=0;j<c2;j++)
            printf("%d ",result[i][j]);
            printf("\n");
    }


    return 0;

}
Transpose Matrix


#include <stdio.h>

int main() {
    int A[10][10],tr[10][10],i, j, r, c;

    printf("Enter number of rows and columns for the matrix: ");
    scanf("%d %d", &r, &c);

    for (i = 0; i < r; i++) {
        for (j = 0; j < c; j++) {
            printf("A [%d] [%d] = ", i, j);
            scanf("%d", &A[i][j]);
        }
    }

        //tranpose
       for (i = 0; i < r; i++)
    {
           for (j = 0; j < c; j++)
            {
            tr[j][i] = A[i][j];
            }
    }

    printf("\n\nFirst Matrix \n");
    for (i = 0; i < r; i++) {
        for (j = 0; j < c; j++)
            printf("%d ", A[i][j]);
        printf("\n");
    }

    //printing tranpose

    printf("\n\nTranpose matrix = \n");
    for (i = 0; i < c; i++)
    {
           for (j = 0; j < r; j++)
            {
            printf("%d ",tr[i][j]);
            }
            printf("\n");
    }


    return 0;
}


Diagonal elements sum


#include<stdio.h>
int main()
{
    int A[10][10],i,j,sum=0;

    printf("Enter the elements of matrix:\n");
    for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            printf("A[%d][%d] = ",i,j);
            scanf("%d",&A[i][j]);
        }
    }
    //output

    printf("Matrix A:\n");
     for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            printf("%d\t",A[i][j]);
        }
        printf("\n");
    }
    //diagonal matrix
         for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            if(i==j)
             {
                sum=sum+A[i][j];
             }
        }
    }
    printf("Sum of Diagonal matrix = %d\n",sum);

    return 0;
}

Sum of upper & lower triangles

#include<stdio.h>
int main()
{
    int A[10][10],i,j,sum=0,uppersum=0,lowersum=0;

    printf("Enter the elements of matrix:\n");
    for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            printf("A[%d][%d] = ",i,j);
            scanf("%d",&A[i][j]);
        }
    }
    //output

    printf("Matrix A:\n");
     for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            printf("%d\t",A[i][j]);
        }
        printf("\n");
    }
    //diagonal matrix
    //printf("Diagonal Elements : ");
             for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            if(i==j)
             {
                sum=sum+A[i][j];
             }
        }
    }

    //upper lower
         for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            if(i<j)
             {
                uppersum = uppersum+A[i][j];
             }
                if(i>j)
             lowersum=lowersum+A[i][j];
             }
        }

    printf("\nSum of Diagonal matrix = %d\n",sum);
    printf("Sum of Upper matrix sum = %d\n",uppersum);
    printf("Sum of Upper matrix sum = %d\n",lowersum);

    return 0;
}



