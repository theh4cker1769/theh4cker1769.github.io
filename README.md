<h1>Binary </h1>

#include <stdio.h>
int main()
{
int i, low, high, mid, n, key, array[100];
printf("Enter number of elementsn");
scanf("%d",&n);
printf("Enter %d integersn", n);
for(i = 0; i < n; i++)
scanf("%d",&array[i]);
printf("Enter value to findn");
scanf("%d", &key);
low = 0;
high = n - 1;
mid = (low+high)/2;
while (low <= high) {
if(array[mid] < key)
low = mid + 1;
else if (array[mid] == key) {
printf("%d found at location %d.n", key, mid+1);
break;
}
else
high = mid - 1;
mid = (low + high)/2;
}
if(low > high)
printf("Not found! %d isn't present in the list.n", key);
return 0;
}

<h1>Insertion </h1>

#include <stdio.h>
int main()
{
    int a[100], number, i, j, temp;
    
    printf("\n Please Enter the total Number of Elements  :  ");
    scanf("%d", &number);
    
    printf("\n Please Enter the Array Elements  :  ");
    for(i = 0; i < number; i++)
        scanf("%d", &a[i]);
    
    for(i = 1; i <= number - 1; i++)
    {
        for(j = i; j > 0 && a[j - 1] > a[j]; j--)
        {
                temp = a[j];
                a[j] = a[j - 1];
                a[j - 1] = temp;
        }
    }
    printf("\n Insertion Sort Result : ");
    for(i = 0; i < number; i++)
    {
        printf(" %d \t", a[i]);
    }
    printf("\n");
    return 0;
}

<h1>Selection </h1>

#include <stdio.h>
int main() {
   int arr[10]={6,12,0,18,11,99,55,45,34,2};
   int n=10;
   int i, j, position, swap;
   for (i = 0; i < (n - 1); i++) {
      position = i;
      for (j = i + 1; j < n; j++) {
         if (arr[position] > arr[j])
            position = j;
      }
      if (position != i) {
         swap = arr[i];
         arr[i] = arr[position];
         arr[position] = swap;
      }
   }
   for (i = 0; i < n; i++)
      printf("%d\t", arr[i]);
   return 0;
}
