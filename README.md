# C
C learning notes

#define _CRT_SECURE_NO_WARNINGS 1

#include <stdio.h>

int main(void)
{

	int arry[5];
	int i,x,n;
	printf("请输入5个数：\n");
	for(i=0;i<5;i++)
		scanf("%d", &arry[i]);

	bubble_sort_arry(arry,5);

	printf("排序好的数组：\n");
	for (i = 0; i < 5; i++)
		printf(" %d", arry[i]);

	printf("\n");
	printf("请输入要查找的数：\n");
	scanf("%d",&x);
	n=binsearch(x, arry,5);
	if (n == 5)
		printf("数据不存在\n");
	else
		printf("该数在排序好的数组的下标为：%d\n", n);
	return 0;
}

int binsearch(int x, int v[],int length)
{
	int i;
	for (i = 0; i < length; i++)
	{
		if (v[i] == x)
			return i;
		
	}
	return i;
}

//冒泡排序
int bubble_sort_arry(int* v, int length)
{
	int i, j;
	int n;
	for (i = 0; i < length; i++)
	{
		
		for (j = 0; j < length - 1; j++)
		{
			if (v[j] > v[j + 1])
			{
				n = v[j];
				v[j] = v[j + 1];
				v[j + 1] = n;
			}

		}
	}
}
