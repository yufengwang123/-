#include<stdio.h>
#include<stdlib.h>
struct GS{
	char name[10];
	int money;
	char timi[20];
	struct yuangong ren;
}a1;
struct  yuangong
{
	char name[20];
	char sex[20];
};
struct GS getincan(struct GS a1)
{
	printf("请输入公司名称：");
	scanf("%s", &a1.name);
	printf("请输入公司市值：");
	scanf("%d", &a1.money);
	printf("请输入公司成立时间：");
	scanf("%s", &a1.timi);
	printf("请输入公司法人信息：");
	scanf("姓名：%s  性别：%s", &a1.ren.name, &a1.ren.sex);
	return a1;
}
void pringet(struct GS a1) {
	printf("该公司的名称为:%s", a1.name);
	printf("该公司的市值为:%d", a1.money);
	printf("该公司成立于:%s", a1.timi);
	printf("该公司的法人为:%s 性别为：%s", a1.ren.name,a1.ren.sex);
}
int main() {
	a1=getincan(a1);
	printf("-----信息录入完毕---");
	pringet(a1);
}
