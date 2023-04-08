# C언어 for문을 이용한 별 찍기
```
#include <stdio.h>
#pragma warning(disable:4996)
int main()
{
	int i, j;

	//5x5사각형
	for (i = 0; i < 5; i++) {
		for (j = 0; j < 5; j++) {
			printf("*");
		}
		printf("\n");
	}
	printf("\n");

	//계단
	for (i = 0; i < 5; i++) {
		for (j = 0; j <= i; j++) {
			printf("*");
		}
		printf("\n");
	}
	printf("\n");

	//역계단
	for (i = 0; i < 5; i++) {
		for (j = 0; j < 5-i; j++) {
			printf("*");
		}
		printf("\n");
	}
	printf("\n");

	//좌우반전계단
	for (i = 0; i < 5; i++) {
		for (j = 0; j < 4 - i; j++) {
			printf(" ");
		}
		for (j = 0; j < i+1; j++) {
			printf("*");
		}
		printf("\n");
	}
	printf("\n");

	//좌우반전역계단
	for (i = 0; i < 5; i++) {
		for (j = 0; j < i; j++) {
			printf(" ");
		}
		for (j = 0; j < 5-i; j++) {
			printf("*");
		}
		printf("\n");
	}

	printf("\n");

	//피라미드
	for (i = 0; i < 5; i++) {
		for (j = 0; j < 4-i; j++) {
			printf(" ");
		}
		for (j = 0; j < 2*i+1; j++) {
			printf("*");
		}
		printf("\n");
	}

	printf("\n");

	//역피라미드
	for (i = 0; i < 5; i++) {
		for (j = 0; j < i; j++) {
			printf(" ");
		}
		for (j = 0; j < (5-i)*2-1; j++) {
			printf("*");
		}
		printf("\n");
	}
	printf("\n");

	//다이아몬드
	for (i = 0; i < 5; i++) {
		for (j = 0; j < 4 - i; j++) {
			printf(" ");
		}
		for (j = 0; j < 2 * i + 1; j++) {
			printf("*");
		}
		printf("\n");
	}
	for (i = 0; i < 4; i++) {
		for (j = 0; j <= i; j++) {
			printf(" ");
		}
		for (j = 0; j < (4 - i) * 2 - 1; j++) {
			printf("*");
		}
		printf("\n");
	}

	

	return 0;
}
```
<h6>배열공부힘드렁</h6>