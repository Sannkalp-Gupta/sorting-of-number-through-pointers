# sorting-of-number-through-pointers
sorted numbers in descending order through pointers


#include<stdlib.h>
#include<stdio.h>
int main()
{
	int n,i,j,t,flag;
	int x[20],*p,*q;
	printf("Enter the number to be sorted=");
	scanf("%d",&n);
	printf("\nEnter %d  values:\n",n);
	i=0;
	while(i<n)
	{
		scanf("%d",&x[i]);
		i++;
	}
	/*Sorting begins */
	i=0;
	q=p=x;
	flag=0;
	while(i<n-1)
	{
		j=0;
		p=q;
		while(j<n-1-i)
		{

			if(*p<*(p+1))
			{
				t=*p;
				*p=*(p+1);
				*(p+1)=t;
				flag=1;
			}
			p++;
			j++;
		}
		if(flag==0)
		{
			break;
		}
		i++;
	}
	p=q;
	i=0;
	printf("\n The number is descending oder are:\n");
	while(p<(q+n))
	{
		printf("%d ",*p);
		p++;
		i++;
	}
	return 0;
}
