# c-study
#define _CRT_SECURE_NO_WARNINGS



#include <stdio.h>


//int main()
//{
//	char ch;
//	while ((ch = getchar()) != '#')
//	{
//		if (ch == '\n')
//			continue;
//		printf("Step 1\n");
//		if (ch == 'c')
//			continue;
//		else if (ch == 'b')
//			break;
//		else if (ch == 'h')
//			goto laststep;
//		printf("Step 2\n");
//	laststep:printf("Step 3\n");
//	}
//	printf("Done\n");
//	return 0;
//}

//    重复输入 到#号结束
//int main()
//{
//	char ch;
//
//	while ((ch = getchar()) != '#')
//		putchar(ch);
//	return 0;
//}

//按指定行列打印字符

//void display(char cr, int lines, int width);
//
//int main()
//{
//	int ch;					/*待打印字符*/
//	int rows, cols;			/*行数和列数*/
//
//	printf("输入一个字符和两个整数:\n");
//	while ((ch = getchar()) != '\n')
//	{
//		if (scanf("%d %d", &rows, &cols) != 2)
//			break;
//		display(ch, rows, cols);
//		while (getchar() != '\n')
//			continue;
//		printf("输入另一个字符和两个整数:\n");
//			printf("输入换行符退出.\n");
//	}
//	printf("拜拜");
//
//	return 0;
//}
//
//void display(char cr, int lines, int width)
//{
//	int row, col;
//
//	for (row = 1; row <= lines; row++)
//	{
//		for (col = 0; col < width; col++)
//			putchar(cr);
//			putchar('\n');   /*结束一行并开始新的一行*/
//	}
//}

#include <stdbool.h>
////输入验证
//// 验证输入是一个整数
//long get_long(void);  
//// 验证范围的上下限是否有效
//bool bad_limits(long begin, long end, long low, long hing);
//// 验证 a~b 的整数平方和
//double sum_squares(long a, long b);
//
//int main()
//{
//	const long MIN = -1000000L;		//范围的下限
//	const long MAX = +1000000L;		//范围的上限
//	long start;						// 用户指定的范围最小值
//	long stop;						// 用户指定的范围最大值
//	double answer;
//
//	printf("这个程序计算一个范围内整数的平方和.\n""下限不下于-10000000\n""上限吧大于+10000000\n""输入 0 表示两个限制都要退出：\n""下限：");
//	start = get_long();
//	printf("上限：");
//	stop = get_long();
//	while (start != 0 || stop != 0)
//	{
//		if (bad_limits(start, stop, MIN, MAX))
//			printf("请再次尝试\n");
//		else
//		{
//			answer = sum_squares(start, stop);
//			printf("整数的平方和");
//			printf("从 %ld 到 %ld 是 %g\n", start, stop, answer);
//		}
//		printf("输入 0 表示两个限制都要退出：\n");
//		printf("上限:");
//		start = get_long();
//		printf("下限:");
//		stop = get_long();
//	}
//	printf("行");
//
//	return 0;
//}
//
//long get_long(void)
//{
//	long input;
//	char ch;
//
//	while (scanf("%ld", &input) != 1)
//	{
//		while ((ch = getchar()) != '\n')
//			putchar(ch);				// 处理错误输入
//		printf("不是一个整数.\n 请进入");
//		printf("整数值例如：25， -178， 或 3：");
//	}
//	return input;
//}
//
//
//double sum_squares(long a, long b)
//{
//	double total = 0;
//	long i;
//
//	for (i = a; i <= b; i++)
//	
//		total += (double)i * (double)i;
//	return total;
//}
//
//bool bad_limits(long begin, long end, long low, long high)
//{
//	bool not_good = false;
//
//	if (begin > end)
//	{
//		printf("%ld 不小于 %ld.\n", begin, end);
//		not_good = true;
//	}
//	if (begin < low || end < low)
//	{
//		printf("值必须是 %ld 或更大.\n", low);
//		not_good = true;
//	}
//	if (begin > high || end > high)
//	{
//		printf("值必须是 %ld 或更少.\n", high);
//		not_good = true;
//	}
//	return not_good;
//}
//

// 菜单程序
//
//char get_choice();
//char get_first();
//int get_int();
//void count();
//
//int main()
//{
//	int choice;
//	while ((choice = get_choice()) != 'q')
//	{
//		switch (choice)
//		{
//		case 'a':
//			printf("接受低价出售高的.\n");
//			break;
//		case 'b':
//			printf('/a');
//			break;
//		case 'c':
//			count();
//			break;
//		default:
//			printf("程序错误");
//			break;
//		}
//	}
//	printf("拜拜.\n");
//
//	return 0;
//}
//
//void count()
//{
//	int n, i;
//
//	printf("输入一个整数：\n");
//	n = get_int();
//	for (i = 1; i <= n; i++)
//		printf("%d\n", i);
//	while (getchar() != '\n')
//		continue;
//}
//
//char get_choice()
//{
//	int ch;
//	printf("输入你的选择：\n");
//	printf("a. 建议          b. 钟\n");
//	printf("c. 计数          q. 退出\n");
//	ch = get_first();
//	while ((ch < 'a' || ch > 'c') && ch != 'q')
//	{
//		printf("请回复a, b, c, 或q.\n");
//		ch = get_first();
//	}
//	return ch;
//}
//
//char get_first()
//{
//	int ch;
//	ch = getchar();
//	while (getchar() != '\n')
//		continue;
//
//	return ch;
//}
//
//int get_int()
//{
//	int input;
//	char ch;
//
//	while (scanf("%d", &input) != 1)
//	{
//		while ((ch = getchar()) != '\n')
//			putchar(ch);
//		printf("不是一个整数.\n 程序错误");
//		printf("整数值例如：25， -178， 或 3：");
//	}
//
//	return input;
//}


// 使用库函数
#include <string.h>

//int main()
//{
//	char arr1[] = "bit";
//	char arr2[20] = "##########";
//	strcpy(arr2, arr1); // strcpy 从字符串中复制字符（函数）
//
//	printf("%s\n", arr2);
//
//	return 0;
//}
//
//int main()
//{
//	char str[] = "almost every programmer should know memset!";
//	memset(str, '-', 6); //memset 替换字符串
//	puts(str);
//	return 0;
//}

//get_max(int x, int y);		/*函数原型*/
//
//int main()
//{
//	int a = 10;
//	int b = 20;
//	int max = get_max(a, b);   /*使用函数*/
//	printf("max = %d", max);
//
//	return 0;
//}
//
//get_max(int x, int y)		/*定义函数*/
//{
//	if (x > y)
//		return x;
//	else
//		return y;
//}

//#define NAME "公司."
//#define ADDRESS "101 金鹰超市"
//#define RLACE "特大城市， CA 94904"
//#define WIDTH 40
//
//void starbar();
//
//int main()
//{
//	starbar();
//	printf("%s\n", NAME);
//	printf("%s\n", ADDRESS);
//	printf("%s\n", RLACE);
//	starbar();
//
//	return 0;
//}
//
//void starbar()
//{
//	int count;
//
//	for (count = 1; count <= WIDTH; count++)
//		putchar("*");
//	putchar('\n');
//}
