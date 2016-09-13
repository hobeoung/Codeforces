# [Codeforces Round #363 (Div. 2)](http://codeforces.com/contest/699)

## [A. Launch of Collider](http://codeforces.com/contest/699/problem/A)

### 문제 설명
문제에 대한 설명을 올립니다
### 코드
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
}
```

## [B. One Bomb](http://codeforces.com/contest/699/problem/B)

### 문제 설명

### 코드
```C++
#include<stdio.h>

int x[1005];
int y[1005];
char str[1005][1005];
int main()
{
	int N, M;
	int cnt = 0;
	scanf("%d %d", &N, &M);
	for (int i = 0; i < N; i++)
	{
		scanf("%s", str[i]);
		for (int j = 0; j < M; j++)
		{
			if (str[i][j] == '*')
			{
				x[i]++;
				y[j]++;
				cnt++;
			}
		}
	}
	for (int i = 0; i < N; i++)
	{
		for (int j = 0; j < M; j++)
		{
			if (str[i][j] == '.') {
				if (x[i] + y[j] == cnt)
				{
					printf("YES\n");
					printf("%d %d", i + 1, j + 1);
					return 0;
				}
			}
			if (str[i][j] == '*') {
				if (x[i] + y[j] - 1 == cnt)
				{
					printf("YES\n");
					printf("%d %d", i + 1, j + 1);
					return 0;
				}
			}
		}
	}
	printf("NO\n");
	return 0;

}
```
