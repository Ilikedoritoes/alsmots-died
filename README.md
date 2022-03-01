#include <stdlib.h>
#include <stdio.h>
#define row 3
#define colume 3
#define _CRT_SECURE_NO_WARNINGS

int main()
{
	int x, y, neg = 0, pos = 0, uneven = 0, even = 0;
	printf("please enter %d x %d numbers.\n", row, colume);
	int mtrx[row][colume];

	for (x = 0; x < row; x++)
	{
		for (y = 0; y < colume; y++)
		{
			scanf_s("%d", &mtrx[x][y]);
		}
	}
	for (x = 0; x < row; x++)
	{
		for (y = 0; y < colume; y++)
		{
			if (mtrx[x][y] % 2 != 0)
				uneven++;
			if (mtrx[x][y] % 2 != 1)
				even++;
			if (mtrx[x][y] >= 0)
				pos++;
			if (mtrx[x][y] > 0)
				neg++;
		}
	}
	
	printf("There was %d even numbers.\n",even);
	printf("There was %d uneven numbers.\n",uneven);
	printf("There was %d negitive numbers.\n",neg);
	printf("There was %d positive numbers.\n",pos);




}
