# Easy-C-file

#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#include <ctype.h>
#include <string.h>
#include <time.h>

void sorted(int a[], int size);
void pickprime(int a[], int size);
int isprime(int x);

int
main(int argc, char *argv[]) {
	srand(time(NULL));
	
	int a[10] = {2,3,4,5,6,7,8,9,10,11};
	int i;
	
	for (i=0;i<10;i++){
		printf("%d\n", a[i]);
	}
	printf("=============\n");
	
	pickprime(a, 10);
	
	
	return 0;
}

void pickprime(int a[], int size){
	int i = 0,j = 0;

	while (i<size){
		if (isprime(a[i])){
			printf("%d\n", a[i]);
		}
		
		i++;
	}
	
}

int isprime(int x){
	int i;
	for (i=2;i*i<=x;i++){
		if (x%i==0){
			return 0;
		}
	}
	return 1;
}
