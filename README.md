# -arr
#include <stdio.h>
int main()
{
	int left = 0, k = 10, mid = 0;
	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
	int sz = sizeof (arr)/sizeof(arr[0]);
	int right = sz - 1;
	
	while (left <= right)
	{
		int mid = (left + right) / 2;
		if (k < arr[mid])
		{
			right = mid - 1;
		}
		else if (arr[mid] < k)
		{
			left = mid + 1;
		}
		else 
		{
			printf("%d", mid);
			break;
		}
		
	}
	if (left > right)
	{
		printf("..." );
	}
	
	return 0;
}
