#include<stdio.h>
#include <stdlib.h>
#include <time.h>
void quicksort(int number[25],int first,int last)
{
   int i, j, pivot, temp;
   if(first<last){
      pivot=first;
      i=first;
      j=last;

      while(i<j)
      {
         while(number[i]<=number[pivot]&&i<last)
            i++;
         while(number[j]>number[pivot])
            j--;
         if(i<j)
         {
            temp=number[i];
            number[i]=number[j];
            number[j]=temp;
         }
      }

      temp=number[pivot];
      number[pivot]=number[j];
      number[j]=temp;
      quicksort(number,first,j-1);
      quicksort(number,j+1,last);

   }
}

int main()
{
   clock_t start,end;
   double timetaken;
   start=clock();
   int i, n;

   printf("Number of Elements: ");
   scanf("%d",&n);
   int arr[n];
   for(i=0;i<n;i++)
    {
        arr[i] = rand() % 100 + 1;
    }

   start=clock();
   quicksort(arr,0,n-1);

   printf("Order of Sorted elements: ");
   for(i=0;i<n;i++)
      printf(" %d",arr[i]);

    end=clock();
    timetaken=((double)(end-start))/CLOCKS_PER_SEC;
    printf("\ntime taken = %f",timetaken);
   return 0;
}
