# 정올 Beginner 문제

1.원하는 구구단의 범위를 입력받아 해당 구간의 구구단을 출력하는 프로그램을 작성하시오

<처리조건>

(1) 구간의 처음과 끝을 입력받는다. 

(2) 입력된 구간은 반드시 처음 입력 값이 끝의 입력 값보다 작아야 하는 것은 아니다. 
(즉 입력된 구간의 범위는 증가하거나 감소하는 순서 그대로 출력되어야 한다.)​ 
```
입력형식:

구구단의 시작 범위 s,와 끝 범위 e를 입력받는다.(s와 e는 2부터 9사이의 정수) 

하나의 결과가 출력되면 프로그램을 종료한다.

출력형식:
시작 범위와 끝 범위사이의 구구단을 출력하되 모든 값과 부호 사이는 공백으로 구분하여 아래 출력 예와 같이 줄을 맞추어 출력해야 한다.

구구단 사이는 3개의 공백으로 구분한다. 

데이터의 크기가 주어진 범위를 벗어날 경우는 "INPUT ERROR!"를 출력하고 s와 e를 다시 입력받는다.
```
```c
	int s, e;
	while (1) {
		scanf("%d %d", &s, &e);
		if ((s <= 9 && s >= 2) && (e <= 9 && e >= 2)) {
			if (s > e) {
				for (int i = 1; i <= 9; i++) {
					for (int j = s; j >= e; j--) {
						printf("%d x %d = %2d   ", j, i, i * j);
					}
					printf("\n");
				}
			}
			else if (e > s) {
				for (int i = 1; i <= 9; i++) {
					for (int j = s; j <= e; j++) {
						printf("%d x %d = %2d   ", j, i, i * j);
					}
					printf("\n");
				}
			}
			break;
		}
		else {
			printf("INPUT ERROR!\n");
			continue;
		}
	}
```
2.원하는 구구단의 범위를 입력받아 해당 구간의 구구단을 출력하는 프로그램을 작성하시오

<처리조건>

(1) 구간의 처음과 끝을 입력받는다. 

(2) 입력된 구간은 반드시 처음 입력 값이 끝의 입력 값보다 작아야 하는 것은 아니다. 
(즉 입력된 구간의 범위는 증가하거나 감소하는 순서 그대로 출력되어야 한다.)
```
입력형식:
구구단의 시작 범위 s와 끝 범위 e가 주어진다. (s와 e는 2부터 9사이의 정수)

출력형식:
시작 범위와 끝 범위사이의 구구단을 출력하되 모든 값과 부호 사이는 공백으로 구분하여 

아래 출력 예와 같이 줄을 맞추어 출력해야 한다.

식과 식 사이는 3개의 공백으로 구분하고 구구단 사이에는 한 줄을 비워 두도록 한다.
```
```c
	int s, e,cnt=0;
	scanf("%d %d", &s, &e);
	if ((s <= 9 && s >= 2) && (e <= 9 && e >= 2)) {
		if (s > e) {
			for (int i = s; i >= e; i--) {
				for (int j = 1; j <= 9; j++) {
					printf("%d x %d = %2d   ", i, j, i * j);
					cnt++;
					if (cnt == 3) {
						printf("\n");
						cnt = 0;
					}
				}
				printf("\n");
			}
		}
		else if (e > s) {
			for (int i = s; i <= e;i++) {
				for (int j = 1; j <= 9; j++) {
					printf("%d x %d = %2d   ", i, j, i * j);
					cnt++;
					if (cnt == 3) {
						printf("\n");
						cnt = 0;
					}
				}
				printf("\n");
			}
		}
	}
```
3.사각형의 높이 n과 너비 m을 입력받은 후 

n행 m열의 사각형 형태로 1부터 n*m번까지 숫자가 차례대로 출력되는 프로그램을 작성하시오.

< 처리조건 > 

숫자의 진행 순서는 처음에 맨 윗줄의 왼쪽에서 오른쪽으로 1부터 차례대로 너비 m만큼 출력한 후 

다음 줄로 바꾸어서 다시 왼쪽에서 오른쪽으로 1씩 증가하면서 출력하는 방법으로 n번 줄까지 반복한다.
```
입력형식:

사각형의 높이n와 너비m( n과 m의 범위는 100 이하의 정수)이 주어진다.

출력형식:

위에서 형태의 직사각형을 입력에서 들어온 높이 n과 너비 m에 맞춰서 출력한다. 숫자 사이는 공백으로 구분한다.
```
```c
int a, b, num = 1;
scanf("%d %d", &a, &b);
for (int i = 1; i <= a; i++) {
	for (int j = 1; j <= b; j++) {
		printf("%2d ", num);
		num++;
	}
	printf("\n");
}
```
4.사각형의 높이 n과 너비 m을 입력받은 후 

사각형 내부에 지그재그 형태로 1부터 n*m번까지 숫자가 차례대로 출력되는 프로그램을 작성하시오. 

< 처리조건 > 

숫자의 진행 순서는 처음에 왼쪽에서 오른쪽으로 너비 m만큼 진행 한 후 방향을 바꾸어서 이를 반복한다. 
```
입력형식:

사각형의 높이n와 너비m( n과 m의 범위는 100 이하의 정수)을 입력받는다.

출력형식:

위에서 형태의 직사각형을 입력에서 들어온 높이 n과 너비 m에 맞춰서 출력한다. 숫자 사이는 공백으로 구분한다.
```
```c
	int a, b,c=1;
	int num[100][100];
	scanf("%d %d", &a, &b);
	for (int i = 0; i < a; i++) {
		if (i % 2 == 0) {
			for (int j = 0; j < b; j++) {
				num[i][j] = c;
				c++;
			}
		}
		else {
			for (int j = b - 1; j >= 0; j--) {
				num[i][j] = c;
				c++;
			}
		}
	}
	for (int i = 0; i < a; i++) {
		for (int j = 0; j < b; j++)
			printf("%2d ", num[i][j]);
		printf("\n");
	}
```
5.정사각형의 한 변의 길이 n을 입력 받은 후 다음과 같이 숫자로 된 정사각형 형태로 출력하는 프로그램을 작성하시오. 

< 처리조건 > 

숫자의 진행 순서는 처음에 왼쪽 위에서 아래쪽으로 n만큼 진행 한 후 

바로 오른쪽 위에서 다시 아래쪽으로 진행하는 방법으로 정사각형이 될 때까지 반복한다.
```
입력형식:

정사각형 한 변의 길이 n(n의 범위는 100 이하의 자연수)을 입력받는다.

출력형식:

위의 형식과 같이 한 변의 길이가 n인 숫자 사각형을 출력한다. 숫자 사이는 공백으로 구분하여 출력한다.
```
```c
	int n,num=1;
	int arr[100][100];
	scanf("%d", &n);
	for (int j = 0; j < n; j++) {
		for (int i = 0; i < n; i++) {
			arr[i][j] = num;
			num++;
		}
	}
	for (int i = 0; i < n; i++) {
		for (int j = 0; j < n; j++)
			printf("%2d ", arr[i][j]);
		printf("\n");
	}
```
6.<a href='http://www.jungol.co.kr/bbs/board.php?bo_table=pbank&wr_id=1316&sca=20'>정올비기너 문자사각형4번 문제</a>

```c
	int n, m,cnt=1,num=1,i,j;
	int arr[100][100];
	scanf("%d %d", &n, &m);
	for (i = 0; i < n; i++) {
		if (m == 1) {
			for (j = 0; j < n; j++)
				arr[i][j] = num;
			num++;
		}
		else if (m == 2) {
			for (i = 0; i < n; i++) {
				if (i % 2 == 0) {
					for (j = 0; j < n; j++) {
						arr[i][j] = num;
						num++;
					}
					num = 1;
				}
				else if (i % 2 == 1) {
					for (j = 0; j < n; j++) {
						arr[i][j] = num + 4;
						num--;
					}
					num = 1;
				}
			}
		}
		else if (m == 3) {
			for (i = 0; i < n; i++) {
				for (j = 0; j < n; j++) {
					arr[i][j] = (i + 1) * (j+1);
				}
			}
		}
	}
	for (i = 0; i < n; i++) {
		for (j = 0; j < n; j++)
			printf("%2d ", arr[i][j]);
		printf("\n");
	}
```