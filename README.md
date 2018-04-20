#include<stdio.h>
#include<string.h>
int main(){
char temp[25];
char *name[] = {"College Station","Houston", "Dallas", "Austin", "San Antonio"};
int i, j, n=5, card = 8;
for (i=0;i<=n;i++)
{
for (j=i+1;j<=n;j++)
{
         if(strcmp(name[i],name[j])>0)
         {
            strcpy(temp,name[i]);
            strcpy(name[i],name[j]);
            strcpy(name[j],temp);
         }
      }
}
   printf("Order of Sorted Strings:");
   for(i=0;i<=n;i++)
        printf("%s\n",name[i]);
}
