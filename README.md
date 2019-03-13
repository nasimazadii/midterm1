//# midterm1
include<stdio.h>

int askUser();
int main()
{
	int r = askUser();
	for (int a = 1; a <= r; a++)
	{
		printf("\t%d", a);
	}
	printf("\n +");
	for (int b = 1; b <= (4 * r); b++)
	{
		printf("-");
	}
	printf("\n");
	int i;
	for (i = 1; i <= r; i++)
	{
		printf("%d|\t", i);
		int j = 1;
		while (!(j > i))
		{
			printf("%d\t", (i*j));
			j++;
		}
		printf("\n");
	}
	for (int c = 1; c < 887; c++); //so that it waits... don't disapper which it did
	getchar();
	return 0;
}

int askUser()
{
	int s; 
	printf("Enter a row/column value:");
	fflush(stdin);
	s = getchar();
	return s;
}
