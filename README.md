#include<stdio.h>
#include<stdlib.h>
#include<time.h>
void emue()
{
printf("******************************\n");
printf("********1>play  0>exit********\n");
printf("********作者:*****************\n");
printf("********宇宙超级大帅哥********\n");
printf("******************************\n");
}
void game()
{
	int net;
int guess;
	int count=0;
	int a=15;

 net=rand()%1000+1;
 
 while(count<=15) 
{
	printf("请猜数:");
 scanf("%d",&guess);
 count++;
 a--;
     if(guess>net)
	 {
	 printf("猜大了\n");
	 printf("还剩%d次机会哦\n",a);
	 }
 else if(guess<net)
 {
	 printf("猜小了\n");
	 printf("还剩%d次机会哦\n",a);
	 }
 else
	{
		
		printf("赢");
     break;
 }
}
 printf("输");
}



int main()
{
	int input;
	srand((unsigned int)time(NULL));//
	do
	{
	 emue();
	printf("请选择:");
	scanf("%d",&input);
	switch(input)
	{case 1:
	        game();
		  break;
	case 0:printf("退出游戏\n");
		  break;
	default:printf("选择错误\n");
		break;}
	}while(input) ;
		return 0;
}
