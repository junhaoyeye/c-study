#include<stdio.h>
// 菜单程序
char get_choice();
char get_first();
int get_int();
void count();
int main()
{
       int choice;
       while ((choice = get_choice()) != 'q')
       {
              switch (choice)
              {
              case 'a':
                     printf("接受低价出售高的.\n");
                     break;
              case 'b':
                     printf('/a');
                     break;
              case 'c':
                     count();
                     break;
              default:
                     printf("程序错误");
                     break;
              }
       }
       printf("拜拜.\n");
       return 0;
}
void count()
{
       int n, i;
       printf("输入一个整数：\n");
       n = get_int();
       for (i = 1; i <= n; i++)
              printf("%d\n", i);
       while (getchar() != '\n')
              continue;
}
char get_choice()
{
       int ch;
       printf("输入你的选择：\n");
       printf("a. 建议          b. 钟\n");
       printf("c. 计数          q. 退出\n");
       ch = get_first();
       while ((ch < 'a' || ch > 'c') && ch != 'q')
       {
              printf("请回复a, b, c, 或q.\n");
              ch = get_first();
       }
       return ch;
}
char get_first()
{
       int ch;
       ch = getchar();
       while (getchar() != '\n')
              continue;
       return ch;
}
int get_int()
{
       int input;
       char ch;
       while (scanf("%d", &input) != 1)
       {
              while ((ch = getchar()) != '\n')
                     putchar(ch);
              printf("不是一个整数.\n 程序错误");
              printf("整数值例如：25， -178， 或 3：");
       }
       return input;
}
