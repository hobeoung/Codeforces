# [Codeforces Round #363 (Div. 2)](http://codeforces.com/contest/699)

## [A. Launch of Collider](http://codeforces.com/contest/699/problem/A)

### 문제 설명

### 코드 추가
```C++
#include<stdio.h>

#define MAXN 200005
#define inf 2000000000

int data[MAXN];
char str[MAXN];

int main()
{
	int N;
	scanf("%d", &N);
	scanf("%s", str);
	for (int i = 0; i < N;i++)
	{
		scanf("%d", &data[i]);
	}
	int min = inf;
	int flag = 0;
	
	for (int i = 0; i < N-1; i++)
	{
		if (str[i] == 'R' && str[i+1] == 'L')
		{
			if (min > (data[i + 1] - data[i]))
			{
				min = data[i + 1] - data[i];
				flag = 1;
			}
		}
	}
	
	if (flag == 0)printf("-1\n");
	else  printf("%d" , (min+1) / 2);
	return 0;
}```
