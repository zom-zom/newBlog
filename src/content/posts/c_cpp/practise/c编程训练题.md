---
title: c编程训练题
published: 2025-02-26
description: ''
image: ''
tags: []
category: '练习题'
draft: false 
lang: ''
---


这是练习题



------



## 编程思维训练一（学会用C语言运算符来表达你的想法）

 

用C表达式来表达下面的题目，比如判断一个整数a是不是等于9，对应的表达式为  a == 9。

### 数学运算

1. 将数学表达式c = 3a + 5b 翻译成C的表达式。

   ``` c
   c = 3*a + 5*b;
   ```

2. 已知某个圆的半径为a，表示圆的面积和圆的周长。

   ``` c
   #define Pi = 3.14	//设定Pi为3.14
   double L = 2 *Pi * a;	//求周长
   double S = Pi * a * a;	//求面积
   ```

3. 已知字符变量a的值对应的是某大写字母，将其转换为对应的小写字母。

   ``` c
   char a = 'A';
   a += 32;	//由于小写字母ASCII码值和大写字母相差32
   ```

4. 获取某个整数a的个位数值（比如75是5，109是9）。

   ``` c
   int a = 75;
   int p1 = a % 10;
   ```

5. 获取某个大于3位的10进制整数a的百位数值（比如1923是9）。

   ``` c
   int a = 1923;
   int p1 = a / 100 % 10;
   ```

6. 假设整数a=1,b=5;表达式a++ + ++b 的值是？

   > a++ + ++b的值为7  a为先使用后加，b为先加后使用

7. 不借助第三个变量，用一组表达式来交换两个整数a和b。

   ``` c
   //加减法
   a = a + b;
   b = a - b;
   a = a - b;
   //异或法
   a = a ^ b;
   b = a ^ b;
   a = a ^ b;
   ```

8. 设变量m,n,a,b,c,d均为0，执行(m=a\==b)||(n=c==d)后，m,n的值是？

   >`==`优先级比`=`高，所以a\==b成立，c==d成立，m和n分别为1。

9. int a=8,b=5,c;, 执行语句 c=a/b+0.4;后,c 的值为？

   > c的值为1

10. 给定一个浮点数，要求将其转化为只保留小数点后2位的小数，其中需要四舍五入，比如1.23678->1.24。

    ``` c
    //方法1直接格式化输出可以四舍五入
    float num1 = 1.23678;
    printf("%.2f\n", num1);
    //方法2
    #include <math.h>
    float num2 = 1.23678;
    float rNum = round(num2 * 100)/100;
    ```





### 逻辑运算

11. 假设a=1,则表达式a=1和a==1的值分别是？

    > 1， 1
    >
    > 表达式a=1则是让给a赋值为1，其值也为1  a==1是a如果等于1则为1,a如果不等为1则为0

12. 假设a=1;表达式!(a-2)的值是？

    > 0
    >
    > 只要非0则为真,去反为0

13. 表达式-1<=3<=-5的值是？

    > 0

14. 假设a=3,b=4,c=5;表达式a+b>c&&b==c的值是？

    > 0

15. 假设a=3,b=4,c=5;表达式!(a>b)&&!c||1的值？

    > 1
    >
    > 逻辑或优先级最低

16. 对于整数a，如果表达式(a%5 == 3) && (a%7\==4)&&(a%5==3)&&(a<20)为真，那么a的值是？

    > 18

17. 判断某个整数a是否能被7整除。

    `if(!(a%7))`

18. 判断某个边长为a的正方形的面积是否比某个半径为b的圆的面积大。

    `if(a*a > 2*b*3.14)`

19. 判断某个正整数a的个位数值在3，8的范围之内。比如16满足，12、19不满足。

    `if(a%10 >=3 && a%10 <=8)`

20. 判断某个字符变量a是不是一个英文字符。 

    ` if(a >= 65 && a <=90 || a >= 97 && a<= 122)`

21. 判断某个字符变量a是不是一个数字字符。

    ` if(a >= 48 && a <= 57)`

22. 判断某个正整数a是不是一个质数（只能被自己和1整除的数）。

    ``` c
    #include <stdbool.h>
    
    bool isPrime(int a) {
    	if (a <= 1) return false; // 1不是质数
    	for (int i = 2; i <= a / 2; i++) {
    		if (a % i == 0) {
    			return false; // 能被整除，不是质数
    		}
    	}
    	return true; // 没有被整除，是质数
    }
    ```

23. 给定整数a，判断它是否能同时被7和3整除。

    `if(!(a%7) && !(a%3))`

24. 给定整数a，判断它是否能被7或者被3整除。

    `if(!(a%7) || !(a%3))`

25. 给定字符a和b，判断它们是否有一个字符是阿拉伯数字符号。

    `if(a >= 48 && a <= 57 || b >= 48 && b <= 57 )`

26. 任意给定某一年为a，判断它是否为闰年。

    `if(!(a%4) && a%100 || !(a%400))`

 

### 逗号运算符

27. 如果有int a; int i = 2;则执行完a = (i++, i++, i++)后;a和i的值分别是？ 

    > a = 4, i = 5;

### 条件运算符

28. 有3个整数a,b,c，不用if只用基本表达式来找到其中的最大值。

    ``` c
    int max = a>b?(a>c?a:c):(b>c?b:c);
    ```

29. 已知:int n,i=1,j=2;执行语句n=i<j?i++:j++;则n、i和j的值是？

    > n=1, i=2, j=2;



 

------



## 编程思维训练二（学会用结构来组织你的想法）

### 分支练习

30. 通过scanf输入一个整数，判断它是否是一个偶数？如果是，则输出这个数。

    ``` c
    int n;
    scanf("%d", &n);
    if(!(n%2))
    	printf("%d",n);
    ```

31. 通过scanf输入一个整数，输出这个整数对应的绝对值。

    ``` c
    int n;
    scanf("%d", &n);
    printf("%d", n > 0 ? n : -n);
    ```

32. 通过scanf输入一个字符，判断它是不是一个大写的英文字符，如果是，则输出这个字符。

    ``` c
    char c;
    scanf("%c", &c);
    if(c >= 65 && c<= 90)
        printf("%c", c);
    ```

33. 通过scanf输入一个字符，判断它是不是一个小写英文字符，如果是则输出这个字符的大写，如果不是则原样输出。

    ``` c
    char c;
    scanf("%c", &c);
    printf("%c", (c >= 97 && c <= 122) ? c - 32 : c);
    ```

34. 通过scanf输入一个字符，判断其是不是一个阿拉伯数字字符，如果是则打印YES否则打印NO。

    ``` c
    char c;
    scanf("%c", &c);
    printf("%s", (c >= 48 && c <= 57) ? "YES" : "NO");
    ```

35. 通过scanf输入代表某一年的整数，如果该年是闰年则输出YES否则输出NO。

    ``` c
    int n;
    scanf("%d", &n);
    printf("%s", (!(n%4) && n%100 || !(n%400))? "YES" : "NO");
    ```

36. 通过scanf输入两个整数，将其中较大的数输出。

    ``` c
    int a, b;
    scanf("%d %d", &a, &b);
    printf("%d", (a > b) ? a : b);
    ```

37. 通过scanf输入三个整数，将其中较小的数输出。

    ``` c
    int a, b;
    scanf("%d %d", &a, &b);
    printf("%d", (a<b)?(a<c?a:c):(b<c?b:c);
    ```

38. 通过scanf输入三个整数，按照从小到大的顺序输出。（采用多重分支）

    ``` c
    int a, b, c;
    scanf("%d %d %d", &a, &b, &c);
    if(a >= b)
        if(b >= c)
            printf("%d %d %d", a, b, c);
    	else
            if(a <= c)
                printf("%d %d %d", c, a, b);
    		else
                printf("%d %d %d", a, c, b);
    else
        if(b >= c)
        	printf("%d %d %d", b, a, c);
    	else
            if(b <= c)
                printf("%d %d %d", c, b, a);
    		else
                printf("%d %d %d", b, c, a);
    ```

39. 通过scanf输入一个3位整数，判断这个数是不是一个对称数，比如757，626等都是。

    ``` c
    int n;
    scanf("%d", &n);
    if (n % 10 == n / 100)
    	printf("Yes\n");
    else
    	printf("No\n");
    ```

40. 给出一个百分制成绩，要求输出成绩等级’A’、’B’、’C’、’D’、’E’。90分以上输出’A’，80～89分输出’B’，70～79分输出’C’，60～69分输出’D’，60分一下输出’E’

    ``` c
    int n;
    scanf("%d", &n);
    if (n>=90)
    	printf("A\n");
    else if(n >= 80 && n<90)
    	printf("B\n");
    else if (n >= 70 && n < 80)
    	printf("C\n");
    else if (n >= 60 && n < 70)
        printf("D\n");
    else
    	printf("E\n");
    ```

41. 有一个函数：

    y = 1; (x <= 1)

    y = x; (x >1 && x < 10)

    y = 2x+1;(x >= 10)

    终端输入x值，编程实现求解该函数的值。

    ``` c
    int func(int x) {
    	if (x <= 1)
    		return 1;
    	else if (x > 1 && x < 10)
    		return x;
    	else if(x >= 10)
    		return 2 * x + 1;
    }
    int main(){
        int x;
        scanf("%d", &x);
        int y = func(x);
        return 0
    }
    ```

42. 输入一个时间，输出它的下一秒时间。比如输入12:30:59秒下一秒是12:31:00。

    ``` c
    int h, m, s;
    scanf("%d:%d:%d", &h, &m, &s);
    if (59 == s)
    	if (59 == m)
    		if (23 == h) {
    			h = 0;
    			m = 0;
    			s = 0;
    		}
    		else {
    			h++;
    			m = 0;
    			s = 0;
    		}
    	else {
    		m++;
    		s = 0;
    	}
    else s++;
    printf("%.2d:%.2d:%.2d\n", h, m, s);
    ```

    



 

>  [!important]
>
>  **分支学完后，以上题目全部可做。**

 

综合练习基础部分（所有人必做）

43. 在屏幕上输出10行内容，每行的内容都是“*”。

    ``` c
    for (int i = 0; i < 10; i++)
    	printf("*\n");
    ```

44. 在屏幕上输出10行内容，每行的内容都是“*****”。

    ``` c
    int i = 0;
    while (i<10){
    	printf("*\n");
    	i++;
    }
    ```

45. 在屏幕上输出10行内容，每行的内容都不一样，第1行一个星号，第2行2个星号，依此类推第10行10个星号。

    ``` c
    for (int i = 0; i < 10; i++)
    {
    	for (int j = 0; j <= i; j++)
    		printf("*");
    	printf("\n");
    }
    ```

46. 在屏幕上输出10行内容，每行的内容都是“1”。

    ``` c
    for (int i = 0; i < 10; i++)
    	printf("1\n");
    ```

47. 在屏幕上输出10行内容，每行的内容都不一样，第1行输出“1”，第2行输出“2”，依此类推第10行输出“10”。

    ``` c
    for (int i = 1; i <= 10; i++)
    	printf("%d\n", i);
    ```

48. 在屏幕上输出以下内容：

    A

     AB

     ABC

     ABCD

     ABCDE

     ABCDEF

    ``` c
    char c = 'A';
    for (int i = 0; i <= 'F'-'A'; i++)
    {
        for (int j = 0; j <= i; j++)
            printf("%c", c+j);
        printf("\n");
    }
    ```

49. 在屏幕上输出以下内容：

    12345

    1234

    123

    12

    1

    ``` c
    for (int i = 5; i > 0; i--)
    {
        for (int j = 1; j <= i; j++)
            printf("%d", j);
        printf("\n");
    }
    ```

50. 计算10个99相加后的值并输出。

    ``` c
    int s = 0;
    for (int i = 0; i < 10; i++)
        s += 99;
    printf("%d\n", s);
    ```

51. 计算从1加到100的值并输出。

    ``` c
    int s = 0;
    for (int i = 1; i <= 100; i++)
        s += i;
    printf("%d\n", s);
    ```

52. 计算10的阶乘（1x2x3x4x5x6x7x8x9x10）。

    ``` c
    int s = 1;
    for (int i = 1; i <= 10; i++)
    	s *= i;
    printf("%d\n", s);
    ```

53. 计算2的20次方。

    ``` c
    int s = 2;
    for (int i = 1; i < 20; i++)
    	s *= 2;
    printf("%d\n", s);
    ```

54. 计算从1到1000以内所有奇数的和并输出。

    ``` c
    int s = 0;
    for (int i = 1; i < 1000; i += 2)
    	s += i;
    printf("%d\n", s);
    ```

55. 计算从1到1000以内所有能被3或者17整除的数的和并输出。

    ``` c
    int s = 0;
    for (int i = 3; i <= 1000; i++) {
    	if (!(i % 3) || !(i % 17))
    		s += i;
    }
    printf("%d\n", s);
    ```

56. 计算从1到1000以内所有能同时被3，5和7整除的数的和并输出。

    ``` c
    int s = 0;
    for (int i = 3; i <= 1000; i++){
        if (!(i % 3) && !(i % 5) && !(i % 7))
            s += i;
    }
    printf("%d\n", s);
    ```

57. 计算1到100以内能被7或者3整除但不能同时被这两者整除的数的个数。

    ``` c
    int s = 0;
    for (int i = 3; i <= 100; i++){
    	if (!(i % 3) || !(i % 7)){
    		if (!(!(i % 3) && !(i % 7)))
    			s += 1;
    	}
    }
    printf("%d\n", s);
    ```

58. 计算1到100以内能被7整除但不是偶数的数的个数。

    ``` c
    int s = 0;
    for (int i = 7; i <= 100; i++){
    	if (!(i % 7)){
    		if (i % 2)
    			s += 1;
    	}
    }
    printf("%d\n", s);
    ```

59. 计算从1到100之间临近两个整数的和并依次输出。比如第一次输出3(1+2)，第二次输出5(2+3)，最后依次输出199(100+99)。

    ``` c
    int s = 0;
    for (int i = 1; i <= 99; i++){
    	printf("%d\n", 2 * i + 1);
    }
    ```

60. 计算从1加到100中途的所有数值的和，比如第一次输出1，第二次输出1+2的和，第3次输出1+2+3的和，最后一次输出1到100所有数相加之后的和。

    ``` c
    for (int i = 1; i <= 100; i++){
    	int s = 0;
    	for (int j = 0; j <= i; j++) {
    		s += j;
    	}
    	printf("%d\n", s);
    }
    ```

61. 判断1077是不是一个质数（质数是只能被1和它自身整除的数）。

    ``` c
    bool isPrime(int a) {
    	if (a <= 1) return false; // 1不是质数
    	for (int i = 2; i <= a / 2; i++) {
    		if (a % i == 0) {
    			return false; // 能被整除，不是质数
    		}
    	}
    	return true; // 没有被整除，是质数
    }
    int main() {
        int n = 1077;
        if (isPrime(n))
            printf("YES");
        return 0;
    }
    ```

62. 一球从100米高度自由落下，每次落地后反跳回原高度的一半；再落下，求它在第10次落地时，共经过多少米？

    ``` c
    float h = 100;
    float s = 0;
    for (int i = 0; i < 10; i++) {
    	s += 3 * h / 2;
    	h /= 2;
    }
    printf("%f\n", s);
    ```

63. 将某个8位的整数所有位的数值加在一起并输出。

    ``` c
    int s = 0;
    int n = 11111111;
    for (int i = 0; i < 8; i++) {
    	s += n % 10;
    	n /= 10;
    }
    printf("%d", s);
    ```

64. 给定一个5位的整数，将该数按照10进制位逆置，例如给定12345变成54321，12320变成2321。

    ``` c
    int s = 0;
    int m = 23400;
    for (int i = 5; i > 0; i--) {
    	int t = 1;
    	for (int j = 1; j < i; j++) {
    		t *= 10;
    	}
    	s += m % 10 * t;
    	m /= 10;
    }
    printf("%d\n", s);
    ```

65. 求s=a+aa+aaa+aaaa+aa...a的值，其中a是一个数字（1-9之间）计算的数据的个数是5。例如2+22+222+2222+22222。

    ``` c
    int s = 0;
    int m = 2;
    for (int i = 1; i <= 5; i++) {
    	int t1 = 0;
    	for (int j = i; j > 0; j--) {
    		int t2 = 1;
    		for (int k = 1; k < j; k++) {
    			t2 *= 10;
    		}
    		t1 += m % 10 * t2;
    	}
    	s += t1;
    }
    printf("%d\n", s);
    ```

66. 给定一个正整数n按照下面的公式计算S(浮点类型)的值。公式：S=1+1/(1+2)+1/(1+2+3)+…….+1/(1+2+3+4+……+n)

    ``` c
    double calc1(int n)
    {
    	double sum = 0;
    	for (int i = n; i > 0; i--)
    	{
    		int t = 0;
    		for (int j = 1; j <= i; j++)
    		{
    			t += j;
    		}
    		assert(t != 0);
    		sum += 1.0 / t;
    	}
    	return sum;
    }
    int main()
    {
        int n = 4;
    	double s = calc1(n);
    	printf("%f", s);
        return 0;
    }
    ```

67. 给定某个字符数组，统计数组中所有英文字符的个数，比如“123fdd”中有3个。

    ``` c
    int countLet(char str[])
    {
    	int sum = 0;
    	int i = 0;
    	while (str[i] != '\0')
    	{
    		if (str[i] >= 65 && str[i] <= 90 || str[i] >= 97 && str[i] <= 122)
    			sum++;
    		i++;
    	}
    	return sum;
    }
    ```

68. 给定某个字符数组，统计数组中所有英文字符和阿拉伯数字的个数，比如“123fdd”中有英文字符有3个，数字3个。

    ``` c
    void countLetNum(char str[], int* sL, int* sN)	//传入字母数量和数字数量的整数指针以便更改 
    {
    	int sumLet = 0;
    	int sumNum = 0;
    	int i = 0;
    	while (str[i] != '\0')
    	{
    		if (str[i] >= 65 && str[i] <= 90 || str[i] >= 97 && str[i] <= 122)
    			sumLet++;
    		else if (str[i] >= 48 && str[i] <= 57)
    			sumNum++;
    		i++;
    	}
    	*sL = sumLet;
    	*sN = sumNum;
    }
    int main(){
        char str[] = "hello123";
        int sL = 0;	//字母数量
        int sN = 0;	//数字数量
        countLetNum(str, &sL, &sN);
        printf("字母数量: %d\n", sL);
        printf("数字数量: %d\n", sN);
        return 0;
    }
    ```

69. 给定某个拥有5个元素的字符数组，数组的成员都有阿拉伯字符构成，试着将该数组转换成一个整数，比如字符数组的内容是：{‘1’,’2’,’3’,’3’,’2’} 则将被转换成12332。

    ``` c
    char str[] = { '1','2','3','3','2' };
    int length = 5;
    int s = 0;
    for (int i = 0; i < length; i++)
    {
    	int t = 1;
    	for (int j = 0; j < length - (i+1); j++)
    	{
    		t *= 10;
    	}
    	s += ((int)str[i]-48) * t;
    }
    printf("%d", s);
    ```

70. 给定一个完全由英文字符构成的数组，将数组中的小写字母转换成大写字母，大写字母转换成小写字母并输出。例如“abcGGG”转化为“ABCggg”。

    ``` c
    void converBigSmallLet(char str[])
    {
    	int i = 0;
    	while (str[i] != '\0')
    	{
    		if (str[i] >= 65 && str[i] <= 90)
    		{
    			str[i] += 32;
    		}
    		else if (str[i] >= 97 && str[i] <= 122)
    		{
    			str[i] -= 32;
    		}
    		i++;
    	}
    }
    int main()
    {
        char str[] = "abcGGG";
        converBigSmallLet(str);
        printf("%s", str);
    	return 0;
    }
    ```

71. 给定一个完全由英文字符构成的数组，将数组中下标为偶数的字符都转换为大写（如果原来是大写则不变）。

    ``` c
    void converBigSmallLetEven(char str[])
    {
    	int i = 0;
    	while (str[i] != '\0')
    	{
    		if (!(i % 2))
    		{
    			if (str[i] >= 97 && str[i] <= 122)
    				str[i] -= 32;
    		}
    		i++;
    	}
    }
    int main()
    {
        char str[] = "abcdefg";
        converBigSmallLetEven(str);
    	printf("%s", str);
    	return 0;
    }
    ```

72. 给一个完全由英文字符构成的字符数组加密，加密原则如下，除了字符‘Z’和‘z’之外，每个字符变成ASCII码值比它大1的字符，也就是‘A’变成‘B’。‘Z’或者‘z’转化为‘A’或者‘a’。

    ``` c
    void lockLet(char str[])
    {
    	int i = 0;
    	while (str[i] != '\0')
    	{
    		if (str[i] >= 65 && str[i] < 90) {
    			str[i] += 1;
    		}
    		else if (str[i] >= 97 && str[i] < 122) {
    			str[i] += 1;
    		}
    		else if (str[i] == 90) {
    			str[i] -= 25;
    		}
    		else if (str[i] == 122) {
    			str[i] -= 25;
    		}
    		i++;
    	}
    }
    ```

73. 计算某个由英文、数字以及标点符号构成的数组的总宽度，其中英文字符的宽度为1cm，数字宽度为0.5cm、标点符号宽度为0.8cm。

    ``` c
    double calcuLen(char str[])
    {
    	int i = 0;
    	double sumLen = 0;
    	while (str[i] != '\0')
    	{
    		if (str[i] >= 65 && str[i] <= 90 || str[i] >= 97 && str[i] <= 122)
    			sumLen += 1;
    		else if (str[i] >= 48 && str[i] <= 57)
    			sumLen += 0.5;
    		else
    			sumLen += 0.8;
    		i++;
    	}
    	return sumLen;
    }
    ```

74. 接上题，如果规定行的宽度为10cm，将某个字符长度超过50的字符串截断，恰好使10cm宽的行能容纳。输出这个被截断的子数组。

    ``` c
    void cutLen(char str[]) {
    	int i = 0;
    	double sumLen = 0;
    	double ratedLen = 10;	//额定宽度10cm
    	while (str[i] != '\0') {
    		if (ratedLen - sumLen >= 1) {
    			if (str[i] >= 65 && str[i] <= 90 || str[i] >= 97 && str[i] <= 122)
    				sumLen += 1;
    			else if (str[i] >= 48 && str[i] <= 57)
    				sumLen += 0.5;
    			else
    				sumLen += 0.8;
    		}
    		else if (ratedLen-sumLen >= 0.8) {
    			if (str[i] >= 48 && str[i] <= 57)
    				sumLen += 0.5;
    			else
    				sumLen += 0.8;
    		}
    		else if (ratedLen - sumLen >= 0.5) {
    			if (str[i] >= 48 && str[i] <= 57)
    				sumLen += 0.5;
    		}
    		else
    			str[i] = '\0';
    		i++;
    	}
    }
    int main() {
        char str[]= "This is a long string that needs to be truncated to fit the width of the line.";
        cutLen(str);
        printf("%s\n", str);
        return 0;
    }
    ```

75. 给定某个整型数组，计算该数组所有偶数的和。

    ``` c
    int calcEvenSum(int arr[], int len) {
    	int sum = 0;
    	for (int i = 0; i < len; i++) {
    		if (arr[i] % 2 == 0) {
    			sum += arr[i];
    		}
    	}
    	return sum;
    }
    int main() {	
    	int arr[] = { 1,2,3,4,2 };
    	int len = sizeof(arr) / sizeof(int);
    	printf("偶数和为%d", calcEvenSum(arr, len));
        return 0;
    }
    ```

76. 给某个整型数组赋值，赋值规律如下，下标能被3整除的都赋值为1，能被5整除的都赋值为2，能被7整除的都赋值为3，能被3、5、7任意两个或者3个都能整除的数赋值为8，其余都赋值为0.

    ``` c
    void assIntArr(int arr[], int len)
    {
    	for (int i = 0; i < len; i++)
    	{
    		if ((i % 3 == 0 && i % 5 == 0) || (i % 3 == 0 && i % 7 == 0) || (i % 5 == 0 && i % 7 == 0))
    			arr[i] = 8;
    		else if (i % 3 == 0)
    			arr[i] = 1;
    		else if (i % 5 == 0)
    			arr[i] = 2;
    		else if (i % 7 == 0)
    			arr[i] = 3;
    		else
    			arr[i] = 0;
    	}
    }
    ```

77. 通过终端输入10个整数并将其保存在一个整型数组中，数字保存在数组中的顺序与下标正好相反，也就是第一个被输入的数放在数组最后一个元素中，最后一个输入的数字放到第一个元素中。

    ``` c
    void backSaveArr(int arr[]) {
    	for (int i = 10; i > 0; i--) {
    		scanf("%d", &arr[i-1]);
    	}
    }
    int main() {
        int arr[10] = { 0 };
        int len = sizeof(arr) / sizeof(int);
        backSaveArr(arr);
    	return 0;	
    }
    ```

78. 通过终端输入10个整数，计算10个整数中所有能被3整除的数的和。

    ``` c
    int temp;
    int sum = 0;
    for (int i = 0; i < 10; i++) {
    	scanf("%d", &temp);
    	if (temp % 3 == 0)
    		sum += temp;
    }
    printf("%d", sum);
    ```

79. 给定一个5个元素构成的整型数组，每个元素的值都在0-9之间，按照位置将其组成一个5位数并输出，例如int a[5] = {1,2,2,3,7};则输出73221。

    ``` c
    int arr[5] = { 1,2,2,3,7 };
    int len = sizeof(arr)/sizeof(int);
    int sum = 0;
    for (int i = len; i > 0; i--) {
    	int t = 1;
    	for (int j = 0; j < i - 1; j++) {
    		t *= 10;
    	}
    	sum += arr[i - 1] * t;
    }
    printf("%d", sum);
    ```

80. 给定2个大小一样的整型数组，将某个数组作为源数组，另一个作为目的数组，然后将源数组的内容拷贝到目的数组。

    ``` c
    int arr[5] = { 1,2,3,4,5 };
    int arr2[5] = { 0 };
    int len = sizeof(arr)/sizeof(int);
    int sum = 0;
    for (int i = 0; i < len; i++) {
    	arr2[i] = arr[i];
    }
    ```

81. 给定一个整型数组，将第一个跟最后一个元素的内容交换。

    ``` c
    int arr[5] = { 1,2,3,4,5 };
    int len = sizeof(arr) / sizeof(int);
    int temp;
    temp = arr[0];
    arr[0] = arr[len - 1];
    arr[len - 1] = temp;
    ```

82. 给定一个整型数组，从第1个元素开始将相邻的两个元素分别相互交换。交换完后，第1个元素将变成最后一个元素，其余元素都前进一位。

    ``` c
    int arr[5] = { 1,2,3,4,5 };
    int len = sizeof(arr) / sizeof(int);
    for (int i = 0; i < len; i++) {
    	if (i != len - 1) {
    		int t = arr[i];
    		arr[i] = arr[i + 1];
    		arr[i + 1] = t;
    	}	
    }
    ```

83. 给定一个有10个整形数的元素，将前5个元素跟后5个元素做整体交换，比如{1,1,1,1,1,2,3,2,2,2}->{2,3,2,2,2,1,1,1,1,1}。

    ``` c
    int arr[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
    int len = sizeof(arr) / sizeof(int);
    for (int i = 0; i < len / 2; i++) {
    	int t = arr[i];
    	arr[i] = arr[i + 5];
    	arr[i + 5] = t;
    }
    ```

84. 判断一个整型数组是否是对称数组，例如{1,2,3,3,2,1}和{1,6,8,1,8,6,1}都是对称数组。

    ``` c
    bool isSym(int arr[], int len) {
    	int i = 0;
    	while (i < len / 2) {
    		if (arr[i] != arr[len - i - 1])
    			return false;
    		i++;
    	}
    	return true;
    }
    int main() {
    	int arr[] = { 1, 2, 3, 4, 5, 4, 3, 2, 1 };
    	int len = sizeof(arr) / sizeof(int);
    	if (isSym(arr, len))
    		printf("YES");
    	else
    		printf("NO");
    	return 0;
    }
    ```

85. 给定两个大小一样的整型数组，交换这两个数组的内容。

    ``` c
    int arr[5] = { 1, 2, 3, 4, 5 };
    int len = sizeof(arr) / sizeof(int);
    int arr2[5] = { 6, 6, 5, 5, 5 };
    int sum = 0;
    for (int i = 0; i < len; i++) {
    	int t = arr[i];
    	arr[i] = arr2[i];
    	arr2[i] = t;
    }
    ```

86. 给定两个大小一样的整型数组，将两个数组中下标一样的元素两两相加，相加后的结果作为这两个数组对应下标的新值，也就是操作完毕后两个数组的内容完全相同。

    ``` c
    int arr[5] = { 1, 2, 3, 4, 5 };
    int len = sizeof(arr) / sizeof(int);
    int arr2[5] = { 6, 6, 5, 5, 5 };
    int sum = 0;
    for (int i = 0; i < len; i++) {
    	int t = arr[i]+ arr2[i];
    	arr[i] = t;
    	arr2[i] = t;
    }
    ```

87. 给定一个能容纳10个元素的整型数组，现有9个元素，现在第5个元素的位置插入一个数字88，后面的数字顺序后移。

    ``` c
    int arr[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9 };
    int len = sizeof(arr) / sizeof(int);
    int t = 0;	//存放在下标为5修改值之前的数据
    int t2 = 0;	//存放后续要修改的值
    for (int i = 5; i <= len; i++) {
        if (i == 5) {
            t = arr[i - 1];		//将第五个元素的值先存储
            arr[i - 1] = 88;
        }
        else {
            t2 = arr[i - 1];	//第六个元素以及后面的都需先存储值然后更改
            arr[i - 1] = t;		//第一次是放入之前第五个原来的值
            t = t2;		       	//t后续存储第六个元素以后的数据
        }
    }
    ```

88. 给定一个10个元素的整型数组，现在将第2个元素删除，后面的数组顺序前移。

    ``` c
    int arr[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 9};
    int len = sizeof(arr) / sizeof(int);
    for (int i = 2; i <= len; i++) {
    	if (i != len)
    		arr[i - 1] = arr[i];
    	else
    		arr[i - 1] = 0;	//将最后空出来的位置初始化
    }
    ```

89. 给定一个有100个元素的数组，查询数组中是否有元素的值等于某个数n。

    ``` c
    bool isContain(int arr[], int len, int findNum)		
    {
    	for (int i = 0; i < len; i++) {
    		if (arr[i] == findNum)
    			return true;
    	}
    	return false;
    }
    ```

90. 给定一个整型数组，求该数组元素中最大值的下标。

    ``` c
    int findMaxSub(int arr[], int len) {
    	int maxNumSub = 0;
    	int maxNum = arr[0];
    	for (int i = 1; i < len; i++) {
    		if (arr[i] > maxNum) {
    			maxNum = arr[i];
    			maxNumSub = i;
    		}
    	}
    	return maxNumSub;
    }
    ```

91. 给定一个整型数组，求该数组中第二大的数的下标。

    ``` c
    int findSecMaxSub(int arr[], int len)
    {
    	int maxNumSub = 0;
    	int secSub = 0;
    	int secNum = 0;
    	int maxNum = arr[0];
    	for (int i = 1; i < len; i++) {
    		
    		if (arr[i] > maxNum)
    		{
    			maxNum = arr[i];
    			maxNumSub = i;
    		}
    		else if(arr[i] > secNum)
    		{
    			secNum = arr[i];
    			secSub = i;
    		}
    	}
    	return secSub;
    }
    ```

92. 给定一个整型数组，求该数组中数值小于10的元素的个数。

    ``` c
    int findNum(int arr[], int len, int num) {	//传入的num就是比较的数，该题为10
    	int sum = 0;
    	for (int i = 1; i < len; i++) {
    		if (arr[i] < num)
    			sum++;
    	}
    	return sum;
    }
    ```

93. 给定一个整型数组，计算大于该数组平均值的元素的个数。

    ``` c
    int calc2(int arr[], int len)
    {
    	int sum = 0;
    	double aver = 0;
    	for (int i = 1; i < len; i++) {
    		aver += arr[i];
    	}
    	aver /= len;
    	for (int i = 1; i < len; i++) {
    		if (arr[i] > aver)
    			sum++;
    	}
    	return sum;
    }
    ```

94. 给定一个整型数组，找到数组中的最小值，并将其放到数组的首元素中，原来首元素的内容放到最小值所在的元素中。

    ``` c
    void exchMinSub(int arr[], int len) {
    	int minNumSub = 0;
    	int minNum = arr[0];
    	for (int i = 1; i < len; i++) {
    		if (arr[i] < minNum) {
    			minNum = arr[i];
    			minNumSub = i;
    		}
    	}
    	int temp = arr[0];
    	arr[0] = minNum;
    	arr[minNumSub] = temp;
    }
    ```

95. 给定一个整型数组，统计某个整数在数组中出现的次数。

    ``` c
    int findNum(int arr[], int len, int num) {	//传入的num就是比较的数
    	int sum = 0;
    	for (int i = 1; i < len; i++) {
    		if (arr[i] == num)
    			sum++;
    	}
    	return sum;
    }
    ```

96. 给定一个英文句子，单词之间用1个空格分开，求出第2个单词的偏移位置。例如“Professor du comes from Korea”的偏移位置是10。

    ``` c
    int findSecOffset(char str[], int len) {
    	int i = 0;
    	while (str[i] != '\0') {
    		if (str[i] == 32)
    			return i+1;
    		i++;
    	}
    	return 0;
    }
    ```

97. 给定一个英文句子，单词之间用1个空格分开，求其中所有单词的数量。

    ``` c
    int countWord(char str[]) {
    	int spacNum = 0;	//空格数量
    	int i = 0;
    	while (str[i] != '\0') {
    		if (str[i] == 32)
    			spacNum++;
    		i++;
    	}
    	return spacNum+1;
    }
    ```

98. 给定两个字符数组，将这两个拼接起来放在第一个数组中（假定第一个数组足够长），比如“abc”和“123”构成“abc123”。

    ``` c
    char str1[10] = "abc";
    char str2[] = "123456";
    int len1 = 0, len2 = 0;	//字符串1和字符串2的长度
    while (str1[len1] != '\0')
    	len1++;	//获取str1的长度
    while (str2[len2] != '\0')
    	len2++;	//获取str2的长度
    int str1Size = sizeof(str1) / sizeof(char);
    if (len2 <= str1Size - len1 - 1)	//判断如果要拷贝字符是否有足够的空间存放,得预留一个位置放'\0'所以多减一
    {
    	for (int i = 0; i < len2; i++)
    	{
    		str1[i + len1] = str2[i];
    	}
    }
    ```

99. 将一个字符数组循环右移2位。比如”12345”->”45123”，假定字符数组中字符的数量大于2.

    ``` c
    ///第一种	循环从前开始
    char str[10] = "123456789";
    int len = 0;
    while (str[len] != '\0')
    	len++;	//获取str的长度
    char t1 = str[0], t2 = str[1];	//存储最初前面两位要位移的字符
    if (len > 2)
    {
    	for (int i = 0; i < len; i++)
    	{
    		if (i == 0)
    			str[0] = str[len - 2];
    		else if (i == 1)
    			str[1] = str[len - 1];
    		else if (i % 2 == 0)	//两个存储的临时变量来回交换
    		{
    			char t = str[i];
    			str[i] = t1;
    			t1 = t;
    		}
    		else
    		{
    			char t = str[i];
    			str[i] = t2;
    			t2 = t;
    		}
    	}
    }
    ///第二种	循环从后开始
    char str[10] = "123456789";
    int len = 0;
    while (str[len] != '\0')
    	len++;	//获取str的长度
    char t1 = str[len - 2], t2 = str[len - 1];	//存储末尾两位要位移的字符
    for (int i = len-1; i >= 2; i--)
    {
    	str[i] = str[i - 2];
    }
    str[0] = t1;
    str[1] = t2;
    ```

100. 给定一个整型数组，数组的长度为N（N>3），从数组中寻找一个连续的长度为3的子数组，要求该子数组的和最大。

     ``` c
     int arr[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
     int len = sizeof(arr) / sizeof(int);
     int maxSum = 0;
     if (len > 3)
     {
     	for (int i = 0; i < len - 2; i++)	//-2是每次要加后面两个数的和
     	{
     		int sum = arr[i] + arr[i + 1] + arr[i + 2];
     		if (maxSum < sum)
     			maxSum = sum;
     	}
     }
     printf("%d", maxSum);
     ```

101. 给定两个长度一样的整型数组，判断两个数组是否相同，相同的原则是数组中的每一个相互对应的元素的“合值”相同，“合值”是指元素对应的整数所有位的和，例如：a[0]的值是1112，b[0]的值是23，则这两个元素“相同”。

     ``` c
     bool arrIsEqual(int *arr1, int *arr2, int len)
     {
     	int sum1 = 0;	//计算每位加起来的合值
     	int sum2 = 0;
     	int tmp = 0;	//临时值，放这不重新开辟空间
     	for (int i = 0; i < len; i++)
     	{
     		tmp = arr1[i];
     		while (tmp)
     		{
     			sum1 += tmp % 10;
     			tmp /= 10;
     		}
     		tmp = arr2[i];
     		while (tmp)
     		{
     			sum2 += tmp % 10;
     			tmp /= 10;
     		}
     		if (sum1 != sum2)
     			return false;
     	}
     	return true;
     }
     ```

102. 给定两个字符数组，比较这两个字符数组的大小，比较的原则是字符数组中所有字符的ASCII值相加后的和值，和值越大则字符数组越大。

     ``` c
     enum compResult {
     	XIANGDENG,
     	XIAOYU,
     	DAYU,
     };
     int compStr(char* str1, char* str2) {
     	int l1 = 0, l2 = 0;	//两条字符串的长度,主要用于遍历
     	int sum1 = 0, sum2 = 0;	//两条字符串所有字符ASCII码值的总和
     	while (str1[l1] != '\0') {
     		sum1 += str1[l1];
     		l1++;
     	}
     	while (str2[l2] != '\0') {
     		sum2 += str2[l2];
     		l2++;
     	}
     	if (sum1 > sum2)
     		return DAYU;
     	else if (sum1< sum2)
     		return XIAOYU;
     	else
     		return XIANGDENG;
     }
     int main() {
         char str1[] = "hello";
         char str2[] = "hello ";
         int val = compStr(str1, str2);
         if (val == DAYU)
             printf("大于");
         else if (val == XIAOYU)
             printf("小于");
         else if (val == XIANGDENG)
             printf("相等");
     }
     ```

     

------



### 综合练习（基础差者选择性做）

103. 在屏幕上输出以下图形：

     ​    \*  

        \***

       \**\***

     ``` c
     int rows = 3;
     for (int i = 1; i <= rows; i++)
     {
     	for (int j = 0; j < rows - i; j++)
     		printf(" ");
     	for (int k = 0; k < 2 * i - 1; k++)
     		printf("*");
     	printf("\n");
     }
     ```

104. 在屏幕上输出以下图形：

     0 1 1 1 1

     -1 0 1 1 1

     -1 -1 0 1 1

     -1 -1 -1 0 1

     -1 -1 -1 -1 0

     ``` c
     int rows = 5;
     for (int i = 0; i < rows; i++)
     {
     	for (int j = 0; j < rows; j++)
     	{
     		if (j > i)
     			printf(" 1 ");
     		else if (j < i)
     			printf("-1 ");
     		else
     			printf(" 0 ");
     	}
     	printf("\n");
     }
     ```

105. 在屏幕上输出以下图形：

     ​       *

     ​      ***

     ​     \**\***

     ​      ***

     ​       *

     ``` c
     int rows = 3;
     for (int i = 1; i <= rows; i++)
     {
     	for (int j = 0; j < rows - i; j++)
     		printf(" ");
     	for (int k = 0; k < 2 * i - 1; k++)
     		printf("*");
     	printf("\n");
     }
     for (int i = rows - 1; i > 0; i--)
     {
     	for (int j = 0; j < rows - i; j++)
     		printf(" ");
     	for (int k = 0; k < 2 * i - 1; k++)
     		printf("*");
     	printf("\n");
     }
     ```

106. 任意给定一个位数不超过9的整数将其所有位的数值加在一起并输出。

     ``` c
     int n = 123456789;
     int sum = 0;
     do 
     {
     	sum += n % 10;
     } while (n/=10);
     printf("%d", sum);
     ```

107. 任意给定一个不超过9位的整数，将其高低位翻转，例如给定12345变成54321，12320变成2321。

     ``` c
     int n = 123456;
     int sum = 0;	//每一位加起来的和
     int t = n;	//临时用于遍历
     do 
     {
     	sum = sum * 10 + t % 10;
     } while (t/=10);
     printf("%d", sum);
     ```

108. 有1、2、3、4个数字，输出所有由这4个数字组成的互不相同且无重复数字的三位数？

     ``` c
     for (int i = 1; i <= 4;i++)
     {
         for(int j = 1;j<=4;j++)
         {
             for (int k = 1; k <= 4; k++)
             {
                 if (i != j && i != k && j != k)
                     printf("%d%d%d ", i, j, k);
             }
         }
     }
     ```

109. 对一个整数进行质因数分解, 例如60可以分解为60 = 2\*2\*3*5。  

     ``` c
     int n = 60;
     while (n % 2 == 0)	//先从2开始
     {
     	printf("2");
     	n /= 2;
     	if (n > 1)
     		printf(" * ");
     }
     for (int i = 3; i <= n / 2; i += 2)	//然后再从其他质数因子处理
     {
     	while (n % i == 0)
     	{
     		printf("%d", i);
     		n /= i;
     		if (n > 1)
     			printf(" * ");
     	}
     }
     if (n > 2)	//如果n还大于2则本身是质数
     	printf("%d", n);
     ```

110. 计算N的阶乘后0的个数。

     ``` c
     int n = 10;
     int fact = 1;
     int coun = 0;
     for (int i = 1; i <= n; i++)
     	fact *= i;
     while (fact)
     {
     	if (fact % 10 == 0)
     		coun++;
     	fact /= 10;
     }
     printf("%d", coun);
     ```

111. 打印出所有的“水仙花数”，所谓“水仙花数”是指一个三位数，其各位数字立方和等于该数。

     ``` c
     for (int i = 100; i < 1000; i++)
     {
     	int cubeSum = 0;
     	int t = i;
     	int s = 0;
     	while (t)
     	{
     		s = t % 10;
     		t /= 10;
     		cubeSum += s * s * s;
     	}
     	if (cubeSum == i)
     		printf("%d ", i);
     }
     ```

112. 有这样一个数列, 这个数列中前两个数为1和1, 从第三个数开始, 每个数都等于前两项之和, 使用循环输出这个数列的前20项。 例如: 1 1 2 3 5 8 13 21 34 ....

     ``` c
     int n = 20;
     int t1 = 1, t2 = 1;	//先将前两位置为1		
     for (int i = 0; i < n; i++)
     {
     	if (i < 2)
     		printf("1 ");
     	else if (i % 2 == 0)
     		printf("%d ", t1 = t1 + t2);
     	else
     		printf("%d ", t2 = t1 + t2);
     }
     ```

113. 一个数如果恰好等于它的因子(除了自身以外的约数)之和, 这个数称为完数, 例如6的因子是1,2,3, 而6=1+2+3, 因此6是完数, 请找出1-1000之内的完数。

     ``` c
     for (int i = 1; i <= 1000; i++)
     {
     	int sum = 0;	//因子和
     	for (int j = 1; j < i; j++)
     	{
     		if (i % j == 0)
     			sum += j;
     	}
     	if (sum == i)
     		printf("%d ", i);
     }
     ```

114. 猴子吃桃问题：猴子第一天摘下若干个桃子，当即吃了一半，还不过瘾，又多吃了一个，第二天早上又将剩下的桃子吃掉一半，又多吃了一个。以后每天早上都吃了前一天剩下的一半零一个。到第10天早上想再吃时，见只剩下一个桃子了。求第一天共摘了多少？

     ``` c
     //此问题可以推算出公式前一天吃的 s = 2n + 2；	n为当前剩的
     int peach = 1;	//当前所剩1
     int d = 0;	//吃了几天
     scanf("%d", &d);
     for (int i = 1; i <= d; i++)
     {
     	peach = 2 * peach + 2;
     }
     printf("%d", peach);
     ```

115. 任意给定一个整型数组，将数组里的元素的顺序倒转过来。

     ``` c
     int arr[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
     int len = sizeof(arr) / sizeof(int);
     for (int i = 1; i <= len/2; i++)
     {
     	int tmp = arr[i-1];
     	arr[i-1] = arr[len - i];
     	arr[len - i] = tmp;
     }
     ```

116. 任意给定一个整型数组，将某一个数字插入到数组的某个位置上（插入后原来数组最后一个元素丢弃）。

     ``` c
     int arr[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
     int len = sizeof(arr) / sizeof(int);
     int pos = 5;	//插入的位置
     int val = 22;	//插入的数值
     int t1 = 0, t2 = 0;	//需要两个变量来存放被覆盖的值
     if (len > pos)
     {
     	for (int i = pos - 1; i < len; i++)
     	{
     		if(i == pos - 1)
     		{
     			t1 = arr[i];
     			arr[i] = val;
     		}
     		else
     		{
     			t2 = arr[i];
     			arr[i] = t1;
     			t1 = t2;
     		}
     	}
     }
     ```

117. 任意给定一个整型数组，删除数组中某一个元素，删除元素后面的元素要依次往前递补。

     ``` c
     int arr[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 9 };
     int len = sizeof(arr) / sizeof(int);
     int pos = 5;	//删除元素的位置
     for (int i = pos; i <= len; i++) {
     	if (i != len)
     		arr[i - 1] = arr[i];
     	else
     		arr[i - 1] = 0;	//将最后空出来的位置初始化
     }
     ```

118. 给定一个按照由小到大排好序的整型数组，快速定位数组中是否有某个整数n。

     ``` c
     int arr[] = { 11, 12, 13, 14, 15 };
     int len = sizeof(arr) / sizeof(int);
     int findNum = 15;
     //先判断是否包含此数
     if (findNum >= arr[0] && findNum <= arr[len - 1])
     	printf("确有此数，下标为: %d", findNum-arr[0]);
     ```

119. 给定一个排序（升序）整型数组，将某个数n插入到该数组中，要求新数组也必须是有序的。

     ``` c
     int arr[] = { 11, 12, 13, 14, 15 };
     int len = sizeof(arr) / sizeof(int);
     int newArr[sizeof(arr) / sizeof(int) + 1] = { 0 };
     int insertNum = 12;
     int i = 0;
     //先查找该插到哪,因为是升序数组所以可以直接比较，如果小就直接插在前面,记录下来要插入的下标.
     for (i; i < len; i++)
     {
     	if (insertNum < arr[i])
     		break;
     }
     printf("%d\n", i);
     //然后赋值给新数组
     for (int j = 0; j < len + 1; j++)
     {
     	if (j < i)
     	{
     		newArr[j] = arr[j];
     	}
     	else if (j > i) 
     	{
     		newArr[j] = arr[j-1];
     	}
     	else
     		newArr[j] = insertNum;
     }
     ```

120. 给定一个整型数组，数组中的元素的值在1-9之间（包括1和9），统计数组中每个元素对应的值出现的次数。比如数组{2,3,2,3,5,6}，2和3分别出现了2次，5和6出现了1次。

     ``` c
     //给定数组元素都在1-9
     int arr[] = { 2, 3, 2, 3, 5, 6 };
     //记录各元素的值出现次数	元素的值对应此数组下标
     int elemCount[10] = { 0 };
     int len = sizeof(arr) / sizeof(int);
     //元素出现，对应此下标值加1
     for (int i = 0; i < len; i++)
     {
     	elemCount[arr[i]]++;
     }
     //次数不为0的输出
     for (int i = 1; i < 10; i++)
     {
     	if (elemCount[i] != 0)
     		printf("%d出现的次数为: %d\n", i, elemCount[i]);
     }
     ```

121. 将两个已排序（升序）的数组合并成一个新数组，合并后的数组也是排好序的。

     ``` c
     //给定两个升序整型数组
     int arr2[] = { 1, 4, 5, 6, 7 };
     int arr1[] = { 1, 2, 3, 8, 9 };
     
     //定义新数组供合并
     int newArr[sizeof(arr1) / sizeof(int) + sizeof(arr2) / sizeof(int)] = { 0 };
     
     int len1 = sizeof(arr1) / sizeof(int);
     int len2 = sizeof(arr2) / sizeof(int);
     
     //排序处理次数为元素总个数	i和j分别遍历两个数组来比较大小
     for (int i = 0, j = 0; i + j < len1 + len2; )
     {
         //需要判断好当有一个数组遍历完了
     	if (i < len1 && (j == len2 || arr1[i] <= arr2[j]))
     		newArr[i + j] = arr1[i++];
     	else
     		newArr[i + j] = arr2[j++];
     }
     ```

122. 将一个整数列按奇数在前偶数在后的顺序重新排列，并要求奇偶两部分分别有序。

     ``` c
     void bubbleSort(int arr[], int len)
     {
     	for (int i = 0; i < len - 1; i++)
     	{
     		for (int j = 0; j < len - i - 1; j++)
     		{
     			if (arr[j] > arr[j + 1])
     			{
     				int tmp = arr[j];
     				arr[j] = arr[j + 1];
     				arr[j + 1] = tmp;
     			}
     		}
     	}
     }
     int main()
     {
         //给定一个数组
         int arr[] = {1, 4, 5, 6, 7, 2, 3, 8, 9};
         const len = sizeof(arr) / sizeof(int);
         //定义两个整型数组来接收奇偶数
         int oddArr[sizeof(arr) / sizeof(int)] = { 1, 4, 5, 6, 7 };
         int evenArr[sizeof(arr) / sizeof(int)] = { 1, 2, 3, 8, 9 };
         //分别记录奇偶数的个数
         int oddNum = 0, evenNum = 0;
         //来遍历给定数组存储奇偶数
         for (int i = 0; i < len; i++)
         {
             if (arr[i] % 2)
                 oddArr[oddNum++] = arr[i];
             else
                 evenArr[evenNum++] = arr[i];
         }
         //排序奇偶数数组	//利用冒泡排序
         bubbleSort(oddArr, oddNum);
         bubbleSort(evenArr, evenNum);
         //定义新数组供合并
         int newArr[sizeof(arr) / sizeof(int) + sizeof(arr) / sizeof(int)] = { 0 };
     	//合并赋值给新数组
     	int k = 0;
     	for (int i = 0; i < oddNum; i++) {
     		newArr[k++] = oddArr[i];
     	}
     	for (int i = 0; i < evenNum; i++) {
     		newArr[k++] = evenArr[i];
     	}
         return 0;
     }
     ```

123. 将某个字符数组中ASCII为偶数的字符全都删除，删除后形成一个新的数组。

     ``` c
     //给定一个字符数组
     char str[] = "abcdefg";
     //求出字符数组大小定义一个新数组
     char newStr[sizeof(str)] = { 0 };
     
     //循环放入ASCII码不为偶数的字符
     int i = 0;
     int j = 0;	//遍历新数组下标
     while (str[i] != '\0')
     {
         if (str[i] % 2)
             newStr[j++] = str[i];
         i++;
     }
     
     printf("%s\n", newStr);
     ```

124. 请计算2的100次方的值并计算有多少个8。

     **使用字符数组模拟手算，逐位保存。相当耗时:rage:借助了ai的思路**

     ```c
     //此题有借助ai完成
     void calc(char* result, int n)
     {
     	result[0] = '1';
     	int len = 1;	//初始长度为1;
     
     	//几次方就需要乘几次
     	for (int i = 0; i < n; i++)
     	{
     		int carry = 0;	//进位，如果计算位数大于10则要进位加
     		for (int j = 0; j < len; j++)
     		{
     			int digit = 2 * (result[j] - '0') + carry;
     			result[j] = digit % 10 + '0';
     			carry = digit / 10;
     		}
     		//如果进位还有值就加到前面的位数上
     		while (carry > 0)
     		{
     			result[len++] = carry % 10 + '0';
     			carry /= 10;
     		}
     	}
     	//重新排序得到正确的数字
     	for (int i = 0; i < len / 2; i++)
     	{
     		char tmp = result[i];
     		result[i] = result[len - i - 1];
     		result[len - i - 1] = tmp;
     	}
     }
     int main()
     {
         char result[500] = {0};
         calc(result, 100);
         int i = 0;
         int count = 0;	//出现指定字符的此数
         while (result[i] != '\0')
         {
             if (result[i] == '8')
                 count++;
             i++;
         }
         printf("2的100次方的值：%s\n", result);
         printf("结果中数字 8 出现的次数为：%d\n", count);
         return 0;
     }
     ```

125. 给定一个英文句子，单词之间用1个或者多个空格分开，求其中所有单词的数量。

     ``` c
     int countWord(char str[]) {
     	int count = 0;	//单词数
     	int i = 0;
     	int inWord = 0;	//标志是否在一个单词中
     	while (str[i] != '\0')
     	{
     		if (str[i] != 32)	//进入单词
     		{
     			if (!inWord)
     			{
     				count++;
     				inWord = 1;
     			}
     		}
     		else
     			inWord = 0;
     		i++;
     
     	}
     	return count;
     }
     ```

126. 将任意一个字符数组循环右移N位。

     ``` c
     void rightMoveStr(char* str, int n) //n为移动位数
     {
     	int len = 0;
     	while (str[len] != '\0')
     		len++;	//获取str的长度
     	n %= len;
     	//外层循环：移动几位循环几次
     	for (int i = 0; i < n; i++)
     	{	
     		char t = str[len - 1];	//存储末尾被覆盖的字符
     		for (int j = len - 1; j > 0; j--)
     		{
     			str[j] = str[j - 1];
     		}
     		str[0] = t;
     	}
     }
     ```

127. 给定一个整数和一个整数数组，从数组里找两个元素，他们的和等于给定的整数。

     ``` c
     void findPairWithSum(int arr[], int n, int sum) {
         for (int i = 0; i < n - 1; i++) {
             for (int j = i + 1; j < n; j++) {
                 if (arr[i] + arr[j] == sum) {
                     printf("找到的两个元素：%d 和 %d\n", arr[i], arr[j]);
                     return;
                 }
             }
         }
         printf("没有找到符合要求的两个元素。\n");
     }
     ```

128. 在一个字符串中找到第一个只出现一次的字符。如输入abaccdeff，则输出b。

     > 思路：循环遍历字符串中每个值，遍历到一个计数器++，然后再用这个值重新遍历字符串中有第二个出现，没有计数器则为1只出现了一次便直接返回字符，如果一直没有计数器为1的字符则返回0。

     ```c
     char findFirstChar(char str[], int len)
     {
     	for (int i = 0; i < len; i++)
     	{
     		char c = str[i];
     		int count = 0;
     		for (int j = 0; j < len; j++)
     		{
     			if (str[j] == c)
     			{
     				count++;
     			}
     		}
     		if (count == 1)
     			return str[i];
     	}
     	return 0;
     }
     
     int main()
     {
     	char str[100];
     	scanf("%s", str);
     	int len = 0;
     	while (str[len] != '\0')
     		len++;
     	char ret;
     	//非0的数则为真，如果找到则返回第一个字符并为真
     	if (ret = findFirstChar(str, len))
     		printf("第一个只出现一次的字符:%c\n", ret);
     	else
     		printf("没有只出现一次的字符");
         return 0;
     }
     ```

129. 给定两个排好序的数组A，B，大小分别为n，m。给出一个高效算法查找A中的哪些元素存在B数组中。

     >思路：因为只查找a中的值，所以定义一个新数组来存储a在b中包含的值，然后循环遍历a的每个值，这个值再在b中遍历是否包含，如果包含则存储在新数组，并用count计数包含的数来表示新数组存储了几个，用作下标遍历。此算法只优化了排好序了所以相同的值会靠在一起，所以只需一个值记录是否上次判断过然后跳过此次去b中判断。算法还不算高效 :smile:

     ```c
     int findContainNum(int arr1[], int arr2[], int findArr[], int len1, int len2)
     {
     	//由于是已经排好序的，所以需要定义一个临时值来判断是否是已经包含了的数
     	int tmp = 0;
     
     
     	int count = 0;	//包含的数的个数，并且用作下标
     	for (int i = 0; i < len1; i++)
     	{
     		//如果是相等的数就跳过
     		if (tmp == arr1[i] && i > 0)
     		{
     			continue;
     		}
     		tmp = arr1[i];
     
     		for (int j = 0; j < len2; j++)
     		{
     			if (arr2[j] == arr1[i])
     			{
     				findArr[count] = arr1[i];
     				count++;
     			}
     		}
     	}
     	//返回包含个数
     	return count;
     }
     
     int main()
     {
     	int arr2[] = { 1, 2, 3, 4, 4, 6, 9 };
     	int arr1[] = { 1, 2, 3, 3, 5, 8, 9 };
     	//找到的数存储
     	int len1 = sizeof(arr1) / sizeof(int);
     	int len2 = sizeof(arr2) / sizeof(int);
     	//只比较数组1的值哪些在数组2里，最坏情况下数组1的值都在数组2里
     	int findArr[sizeof(arr1) / sizeof(int)];
     	int count = findContainChar(arr1, arr2, findArr, len1, len2);
     	printf("A中包含的元素有: ");
     	for (int i = 0; i < count; i++)
     	{
     		printf("%d ", findArr[i]);
     	}
         return 0;
     }
     ```

     

130. 输入两个字符串，从第一字符串中删除第二个字符串中所有的字符。例如，输入”They are students.”和”aeiou”，则删除之后的第一个字符串变成”Thy r stdnts.”。

     > 思路：依旧是定义一个新字符数组，然后查找有没，如果没有则赋值。然后记录赋值了几个值，并用作下标遍历。

     ```c
     #include <string.h>
     #include <stdio.h>
     int findNoContainChar(char str1[], char str2[], char newStr[], int len1, int len2)
     {
     	int count = 0;	//不包含的数的个数，并且用作下标
     	bool isContain;	//用来记录是否包含，如果包含则false不赋值
     	for (int i = 0; i < len1; i++)
     	{
     		isContain = false;
     		//遍历是否包含值，如果包含将isContain置为true，跳出循环
     		for (int j = 0; j < len2; j++)
     		{
     			if (str2[j] == str1[i])
     			{
     				isContain = true;
     				break;
     			}
     		}
     		if (!isContain)
     		{
     			newStr[count] = str1[i];
     			count++;
     		}
     	}
     	//将新数组最后一个元素的下个元素置为\0
     	newStr[count + 1] = '\0';
     
     	//返回包含个数
     	return count;
     }
     
     int main()
     {
     	//没有找的字符存储
     	char str1[100] = {0};
     	char str2[100] = {0};
     	char newStr[100] = {0};
     	//将输入的字符串存储到str1和str2中，第二参数为最大输入长度，第三个参数为输入流
     	//fgets解决了scanf的问题，scanf遇到空格就会停止读取，而fgets可以读取空格，不过scanf([^\n], str)可以读取空格但是会遗留\n在输入流中
     	fgets(str1, 100, stdin);
     	fgets(str2, 100, stdin);
     	int len1 = strlen(str1);
     	int len2 = strlen(str2);
     	int count = findNoContainChar(str1, str2, newStr, len1, len2);
     	printf("newStr: %s", newStr);
     	return 0;
     }
     ```

     

131. 给定一个字符数组，判断某个字符串是否在这个字符数组中，比如“abdefghj78”中包含“defg”。

     > 思路：先遍历给的字符数组，然后判断是否找到了子串中的第一个字符，然后从这个字符开始遍历，遍历是否后续都相等，其中遍历的时候给一个布尔变量，如果判断有一个不相等赋值false并跳出循环，接着继续找和子串第一个字符相等的字符开始遍历。

     ```c
     bool isContainSubStr(char str1[], char str2[], int len1, int len2)
     {
     	bool isContain = false;
     	for (int i = 0; i < len1; i++)
     	{
     		if (str1[i] == str2[0])
     		{
     			//包含第一个子串字符则首先设为真
     			isContain = true;
     			//遍历子串的每一个字符与主串的字符进行比较
     			for (int j = 0; j < len2; j++)
     			{
     				if (str2[j] != str1[i + j])
     				{
     					isContain = false;
     					break;
     				}
     			}
     			if (isContain)
     				return true;
     		}
     	}
     
     	
     	return false;
     }
     
     int main()
     {
     	char str1[100] = {0};
     	char str2[100] = {0};
     	char newStr[100] = {0};
     	
     	scanf("%[^\n]", &str1);
     	getchar();
     	scanf("%[^\n]", &str2);
     	fgets(str1, 100, stdin);
     	fgets(str2, 100, stdin);
     
     	int len1 = strlen(str1);
     	int len2 = strlen(str2);
     	if (isContainSubStr(str1, str2, len1, len2))
     		printf("YES,Contain!");
     	else
     		printf("Not Contain");
         return 0;
     
     }
     ```

     

132. 给定一个整型数组，统计数组中每个元素对应的值出现的次数。比如数组{2,3,2,3,5,6}，2和3分别出现了2次，5和6出现了1次。

     > 思路：不动态开辟数组，考虑到最坏情况数组每个元素都存在一次，所以定义一个二维数组其一维长度与数组长度相同，用来记录每个值的出现次数。接着遍历数组的每个值，以及判断是否存在于二维记录数组中，再定义一个变量来计数存放了几个用作下标。如果不存在则存入并使计数变量+1。最后用计数变量来遍历二维数组打印各值出现了几次。由于数组初始化为0还得考虑0出现的次数，所以先将0计算并记录随后记录其他值。    —这题是真耗时间啊:smiling_imp: 

     ```c
     int countArrNum(int arr[], int (*statisticTab)[2], int len)
     {
     	//二维数组记录值的次数
     	int count = 0;
     	bool isRecord = false;
     	//首先存放0的问题，因为存放数组初始化为0考虑到数组内有0数字，得先遍历0然后存储方便后续比较是否有记录过的值
     	//定义0出现的次数
     	int count0 = 0;
     	for (int i = 0; i < len; i++)
     	{
     		if (arr[i] == 0)
     			count0++;
     	}
     	//如果0出现次数大于1则记录
     	if (count0)
     	{
     		statisticTab[count][0] = 0;
     		statisticTab[count][1] = count0;
     		count++;
     	}
     	//定义其他各个数字出现的次数
     	int countNum = 0;
     	//遍历数组中每个数，并将每个数再遍历得到出现次数
     	for (int i = 0; i < len; i++)
     	{
     		//每个被遍历的值都先设为没有被记录以及出现次数为0
     		isRecord = false;
     		countNum = 0;
     
     		//判断值是否被记录过
     		for (int j = 0; j < count; j++)
     		{
     			if (statisticTab[j][0] == arr[i])
     			{
     				isRecord = true;
     			}
     		}
     		//若被记录过直接跳过不再查找这次要找的值
     		if (isRecord)
     			continue;
     
     		//查找没被记录过的值出现次数
     		for (int j = 0; j < len; j++)
     		{
     			if (arr[j] == arr[i])
     				countNum++;
     		}
     
     		//如果没记录过就存入 这里判不判断都行，前面已经判断过如果记录了直接跳到下次循环了
     		if (!isRecord)
     		{
     			statisticTab[count][0] = arr[i];
     			statisticTab[count][1] = countNum;
     			count++;
     		}
     	}
     	return count;
     }
     
     int main()
     {
     	
     	int arr[] = { 2, 3, 2, 3, 5, 6, 0, 0, 2, 0 };
     	int len = sizeof(arr) / sizeof(arr[0]);
     	//定义存储变量和次数的二维数组
     	int statisticTab[sizeof(arr) / sizeof(int)][2] = { 0 };
     	//定义一个二维数组指针	...这里练习一下二维数组指针定义
     	int (*p)[2] = statisticTab;
     	//返回的值是二维数组里面记录的元素个数
     	int count = countArrNum(arr, p, len);
     
     	for (int i = 0; i < count; i++)
     	{
     		printf("%d出现的次数为： %d次\n", statisticTab[i][0], p[i][1]);
     	}
         return 0;
     }
     ```

     

133. 两个兵乓球队进行比赛, 各出三人, 甲队为A,B,C三人, 乙队为X,Y,Z三人, 已抽签决定比赛名单, 有人向队员打听比赛的名单, A说他不和X比, C说他不和X,Z比, 请编写程序找出三队赛手的名单。

     > 思路：将ABC和XYZ分别用整数替代对应的赛程场次。设定总共赛程1,2,3这3个值，首先将甲队ABC三人场次先分别设为1,2,3，接着将乙队的每个人假设一个赛程场次进行判断，初始条件为C不和X、Z一个赛程，那么C和Y一个赛程即C=Y。A不和X，Y又和C一个场次那么A和Z一个场次即A=Z；
     > 编程需要来一个判断条件，判断是否有三队都相等的，如果没有则重新赋值判断。赋值过程A不能等于X，C不能等于X和Z。    –手写画图更简单 :smiling_imp: 

     ```c
     bool setSchedule(const int a,const int b,const int c, int* x, int* y, int* z)
     {
     	//定义一个是否设置好了三名人员的场次的布尔变量
     	bool isFindRightSet = false;
         //这里也定义一个是否有多次设置人员场次的情况
         int count = 0;
     	//首先给三个数进行赋值,这里给乙队进行赋值，乙队的第一个成员X开始从1开始赋值到3，如果内部条件三个场次的人都能匹配上并且不相同则退出函数。
     	for (int i = 1; i <= 3; i++)
     	{
     		*x = i;
     		for (int j = 1; j <= 3; j++)
     		{
     			//j不能等于i因为y队同队人员不能赋值同一个场次，必须是一个单独的场次
     			if (j != i)
     			{
     				*y = j;
     				for (int k = 1; k <= 3; k++)
     				{
     					//k不能等于i和j因为y队同队人员不能赋值同一个场次，必须是一个单独的场次
     					if (k != i && k != j)
     					{
     						*z = k;
     						//此时条件满足乙队三个人都在不同的场次
     						//然后进行条件判断是否满足A、C两人所说的条件	a不能等于x， c不能等于x和z,此时已经确保了三人都在不同的场次
     						if (a != *x && c != *x && c != *z)
     						{
     							isFindRightSet = true;
     							count++;
     						}
     					}
     				}
     			}
     		}
     	}
         if(count>1)
         	printf("出现了多次可以匹配对手的场景\n");
     	return isFindRightSet;
     }
     
     int main()
     {
     	const int A = 1, B = 2, C = 3;
     	int X = 0, Y = 0, Z = 0;
     	//判断是否有匹配成功
     	if (setSchedule(A, B, C, &X, &Y, &Z))
     	{
     		//现在乙队的场次分配好了只需对照场次便能找到对手
     		printf("A的场次为%d，B的场次为%d，C的场次为%d\n", A, B, C);
     		printf("X的场次为%d，Y的场次为%d，Z的场次为%d\n", X, Y, Z);
     	}
     	return 0;
     }
     ```

     

134. 返回一个整数数组的连续子数组，该子数组的和在所有连续子数组里和最大。例如，[−2,1,−3,4,−1,2,1,−5,4], 子数组[4,−1,2,1] 是符合该要求的最大子数组。

     > 思路：查阅了一下资料，单个数和整个数组本身理应也算作连续子数组。首先需要定义一个数组来接收每一次的连续子数组，考虑到整个数组本身是最大连续子数组和的情况下，需要定义一个与数组长度相等的数组来接收目前找到的最大子数组，并记录子数组元素的个数方便后续遍历输出，并且还记录目前最大子数组和的大小，然后再定义一个数组用来接收每一次临时组成的子数组，与目前找到的最大子数组进行比较，如果更大，则把当前子数组的元素依次赋值给最大子数组，并利用记录子数组元素的变量用作循环控制条件，使没有记录的下标位置赋值为0初始化一下，之前的最大子数组可能给其他下标位置赋值了。然后函数结束最大子数组已被设置好。

     ```c
     //计算数组的和
     int sumArr(int arr[], int len)
     {
     	int sum = 0;
     	for (int i = 0; i < len; i++)
     		sum += arr[i];
     	return sum;
     }
     
     int findMaxSubArr(int arr[], int len, int maxSubArr[], int tmpArr[])
     {
     	//初始第一次最大子串就设为第一个单数
     	int countMaxSubArr = 0;
     	maxSubArr[countMaxSubArr] = arr[0];
     	countMaxSubArr++;
     	//定义每次记录最大子串的和，初始化为第一个单数
     	int maxSubArrSum = arr[0];
     
     	//定义临时组成子串的元素个数
     	int countTmpSubArr = 0;
     	//定义临时组成子串变量的和
     	int tmpSubArrSum = 0;
     
     	//然后开始遍历，开始组成子串，先组成单数
     	for (int i = 0; i < len; i++)
     	{
     		//遍历完重新初始化临时组成子串
     		for (int j = 0; j < countTmpSubArr; j++)
     		{
     			tmpArr[j] = 0;
     		}
     		countTmpSubArr = 0;
     		tmpSubArrSum = 0;
     		// 假设数组为[a, b, c, d, e]
     		// 第一次循环不断变成 a -> a,b -> a,b,c -> a,b,c,d,e; 并且每一次组成都会与记录的最大值比较
     		// 第二次循环不断变成 b -> b,c -> b,c,d -> b,c,d,e; 这里第二轮不需要从a开始是因为第一轮从a开始的值都已经比较过
     		// 让临时组成子串不断组成更大的连续子串
     		for (int j = i; j < len; j++)
     		{
     			tmpArr[countTmpSubArr] = arr[j];
     			countTmpSubArr++;
     			//组成完成后立即打印 用于调试查看是否有组成
     			//for (int k = 0; k < countTmpSubArr; k++)
     			//{
     			//	printf("%d ", tmpArr[k]);
     			//}
     			//printf("\n");
                 
     			//使组成的连续子串与目前最大的连续子串进行比较
     			tmpSubArrSum = sumArr(tmpArr, countTmpSubArr);
     			if (tmpSubArrSum > maxSubArrSum)
     			{
     				//如果临时子串和更大则将临时子串全部赋值给最大子串	其中其余位置全部赋值为0初始化
     				for (int k = 0; k < len; k++)
     				{
     					if (k < countTmpSubArr)
     						maxSubArr[k] = tmpArr[k];
     					else
     						maxSubArr[k] = 0;
     				}
     				maxSubArrSum = tmpSubArrSum;
     				countMaxSubArr = countTmpSubArr;
     			}
     			else if (tmpSubArrSum == maxSubArrSum)
     				printf("发生相等的情况,在子串首数字为:%d, 尾数字为:%d, 长度为: %d时\n", maxSubArr[0], maxSubArr[countMaxSubArr - 1], countMaxSubArr);
     		}
     	}
     	return countMaxSubArr;
     }
     
     void test1()
     {
     	//首先计算好长度定义好各数组
     	int arr[] = { -2, 1, -3, 4, -1, 2, 1, -5, 4 };
     	int len = sizeof(arr) / sizeof(arr[0]);
     	int maxSubArr[sizeof(arr) / sizeof(arr[0])] = { 0 };
     	int tmpArr[sizeof(arr) / sizeof(arr[0])] = { 0 };
     
     	int count = findMaxSubArr(arr, len, maxSubArr, tmpArr);
     	printf("最大连续子串为: ");
     	for (int i = 0; i < count; i++)
     		printf("%d ", maxSubArr[i]);
     	printf("\n最大连续子串和为：%d", sumArr(maxSubArr, count));
     
     }
     ```

     下面是这道题的调试运行输出结果，加了一点调试功能，在组成临时子串后打印临时子串查看是否组成，然后并判断其他连续子串是否有相等现在最大子串的情况

     ```c
     -2
     发生相等的情况,在子串首数字为:-2, 尾数字为:-2, 长度为: 1时
     -2 1
     -2 1 -3
     -2 1 -3 4
     -2 1 -3 4 -1
     -2 1 -3 4 -1 2
     -2 1 -3 4 -1 2 1
     -2 1 -3 4 -1 2 1 -5
     -2 1 -3 4 -1 2 1 -5 4
     1
     1 -3
     1 -3 4
     发生相等的情况,在子串首数字为:-2, 尾数字为:1, 长度为: 7时
     1 -3 4 -1
     1 -3 4 -1 2
     1 -3 4 -1 2 1
     1 -3 4 -1 2 1 -5
     1 -3 4 -1 2 1 -5 4
     -3
     -3 4
     -3 4 -1
     -3 4 -1 2
     -3 4 -1 2 1
     -3 4 -1 2 1 -5
     -3 4 -1 2 1 -5 4
     4
     发生相等的情况,在子串首数字为:1, 尾数字为:1, 长度为: 6时
     4 -1
     4 -1 2
     4 -1 2 1
     4 -1 2 1 -5
     4 -1 2 1 -5 4
     -1
     -1 2
     -1 2 1
     -1 2 1 -5
     -1 2 1 -5 4
     2
     2 1
     2 1 -5
     2 1 -5 4
     1
     1 -5
     1 -5 4
     -5
     -5 4
     4
     最大连续子串为: 4 -1 2 1
     最大连续子串和为：6
     ```
