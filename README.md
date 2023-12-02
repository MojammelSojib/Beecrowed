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

