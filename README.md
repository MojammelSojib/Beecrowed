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
