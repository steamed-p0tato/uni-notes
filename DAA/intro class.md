1.
```C
for (i = 1; i<=3; i++){
	for (j=1;j<=3;j++){
		if(i!=j)
		break;
		else
		printf("\n %d%d", i,j);
		}
}

```
ans- 11

2.
```C
for (i = 1; i<=3; i++){
	for (j=1;j<=3;j++){
		if(i==j)
		break;
		else
		printf("\n %d%d", i,j);
		}
}

```
ans- 21, 31, 32

3.
```C
for (i = 1; i<=3; i++){
	for (j=1;j<=3;j++){
		if(i!=j)
		continue;
		else
		printf("\n %d%d", i,j);
		}
}

```
ans- 11, 22, 33

Q wacp to check 
1. weather a given no. is unique no or not
2. to print all the unique numbers between the range 1 - 10
3. wacp to find amicable no.
4. wacp to check if a number is krishnamurti number or not


```c
#define sqr(x) (x*x)
void main ()
{
	int a,b= 3;
	a = sqr(b+2);
	pf("\n %d", a);
}
```
ans is 11


```c
#define MAX(x,y)((x)>(y))?(x):(y)
void main(){
int i = 10,j,k;
j = 5;
k = 0;
k = MAX(++i, j++);
pf("%d %d %d", i,j,k);
}
```
and is  12 6 12
