# OpenSourceWeekend
//Day 2 activity of Open Source Weekend organised by xxCode team for women developers 
#include<stdio.h>
 
int main() {
   int a[100], i, j, k, size;
 
   printf("\nEnter array size : ");
   scanf("%d", &size);
 
   printf("\nenter  Numbers : ");
   for (i = 0; i < size; i++)
      scanf("%d", &a[i]);
 
   printf("\nArray with no duplicate elements : ");
   for (i = 0; i < size; i++) {
      for (j = i + 1; j < size;) {
         if (a[j] == a[i]) {
            for (k = j; k < size; k++) {
               a[k] = a[k + 1];
            }
            size--;
         } else
            j++;
      }
   }
 
   for (i = 0; i < size; i++) {
      printf("%d ", a[i]);
   }
 
   return (0);
}