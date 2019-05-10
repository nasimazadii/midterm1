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
//Question #3: updated on 05.09.2019
#include<string>
#include<iostream>

using namespace std;

class A
{
	int size;
	float* p;
public:
	A(int s)
	{
		size = s;
		p = new float[s];
	}
	~A()
	{
		delete p;
	}
	void locateValue_At(int loc, int value)
	{
		if (loc < size && loc>0)
			*(p + loc) = value;
		else
			cout << "input boundary is out of range " << endl;
	}

	float getValue_At(int location) const
	{
		float *l = (p + (location * sizeof(float)));
		return *l;
	}

	float Max()
	{
		float max = p[0];
		for (int a = 0; a < size; a++)
		{
			if (p[a] > max)
				max = p[a];
		}
		return max;
	}

	float Min()
	{
		float min = p[0];
		for (int a = 0; a < size; a++)
		{
			if (p[a] < min)
				min = p[a];
		}
		return min;
	}

};
