<h1>C언어 제어문을 이용한 코드</h1>

1. 소문자 aabbcc등이 차례대로 입력되면 대문자로 바꾸어 주는 코드

```c
	char c;
	while (1) {
		scanf("%c", &c);
		if (c == '\n')
			break;
		else if (c >= 'a' && c <= 'z')
			c -= 32;
		printf("%c", c);
	}
```
2. 숫자 데이터를 계속 입력 받다가 0을 입력받으면 정지하고 그전까지의 데이터중 최솟값을 출력하는 코드

```c
	int i, max = 1000000;
	for (i = 1; i != 0;)
	{
		printf("데이터를 입력하시오(0을 입력하면 종료)");
		scanf("%d", &i);
		if (i == 0)
			break;
		else if (i < max)
			max = i;
	}
	printf("%d", max);
```
3. 숫자를 입력받고 약수와 약수의 갯수를 출력해주는 코드

```c
	int i, yac, cnt = 0;
	scanf("%d", &yac);
	for (i = 1; i <= yac; i++) {
		if (yac % i == 0) {
			printf("%d ", i);
			cnt++;
		}
	}
	printf("약수의 갯수는 %d개입니다.", cnt);
```
4. 두 수를 입력받고 두 수의 최대공약수와 최소공배수를 출력해주는 코드

```c
	int a =1, b =1, r =1, mul;
	printf("input numbers>>");
	scanf("%d %d", &a, &b);
	mul = a * b;
	while (b != 0) {
		r = a % b;
		a = b;
		b = r;
	}
	printf("최대공약수 : %d\n", a);
	printf("최소공배수 : %d", mul / a);
```
