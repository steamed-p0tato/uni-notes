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
