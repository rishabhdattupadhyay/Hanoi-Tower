# Hanoi-Tower
Object of the game is to move all the disks over to Tower 3 (with your mouse). But you cannot place a larger disk onto a smaller disk.
#include<stdio.h>
void  tower(int n , char s, char h, char d){
	if(n==0) return;
	tower(n-1,s,h,d);
	printf("%c -> %c\n",s,d);
	tower(n-1,h,s,d);
	return ;
}
int main(){
	int n;
	printf("Enter the number of disk");
	scanf("%d",&n);
	tower(n,'A','B','C');
	return 0;
}
