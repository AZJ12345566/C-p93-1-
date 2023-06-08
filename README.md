# C-p93-1-
C语言学习笔记 p93数组(1)
//本章重点
//1.一维数组的创建和初始化
//2.一维数组的使用
//3.一维数组在内存中的存储
//4.二维数组的创建和初始化
//5.二维数组的使用
//6.二维数组在内存中的存储
//7.数组作为函数参数
//8.数组的应用实例1:三字旗
//9.数组的应用实例2:扫雷游戏

//一维数组的创建
#include<stdio.h>
#include<string.h>
int main()
{
    //创建一个数组-存放整形-10个
    int arr[10];
    //创建一个数组-存放字符-5个
    char arr2[5];
    
    //int n=5;
    //char ch[n];//这种写法是错误的，指定数组的大小必须用一个常量表达式
    return 0;
}

//一维数组的初始化
int main()
{
    int arr[10]={1,2,3};//不完全初始化，剩下的元素默认初始化为0
    char arr2[5]={'a','b'};//也是不完全初识化，剩下元素默认为0
    char arr4[5]={'a',98};//这样是可以的，输出为a，b，0，0，0. 98就是b
    char arr3[5]="ab";//这样初始化也是可以的，后面三个元素默认为0
    char arr5[]="abcdef";
    printf("%d\n",sizeof(arr5);//7
    //sizeof计算arr4所占空间的大小
    //7个元素-char 7*1=7
    printf("%d\n",strlen(arr5);//6
    //strlen求字符串的长度
    
    return 0;
}
//1.strlen和sizeof没有关联
//2.strlen是求字符串长度的-只能针对字符串求长度-库函数-使用得引头文件
//3.sizeof计算变量，数组，类型的大小-单位是字节-操作符

int main()
{
    char arr1[]="abc";
    char arr2[]={'a','b','c'};
    printf("%d\n"sizeof(arr1));//4
    printf("%d\n"sizeof(arr2));//3
    printf("%d\n"strlen(arr1));//3
    printf("%d\n"strlen(arr2));//随机数
    return 0;
}

//一维数组的使用
int main()
{
    char arr[]="abcdef";//[a][b][c][d][e][f][\0]
    //printf("%c\n",arr[3]);
    int i=0;
    int len=strlen(arr)
    for(i=0;i<len;i++)
    {
        printf("%c",arr[i]);
    }//输出abcdef
    return 0;
}
int main()
{
    int arr[]={1,2,3,4,5,6,7,8,9,0};
    int sz=sizeiof(arr)/sizeof(arr[0]);
    int i=0;
    for(i=0;i<sz;i++)
    {
        printf("%d",arr[i]);
    }
    return 0;
}

//一维数组在内存中的存储
int main()
{
    int arr[]=(1,2,3,4,5,6,7,8,9,10};
    int sz=sizeof(arr)/sizeof(arr[0]);
    int i=0;
    for(i=0;i<sz;i++)
    {
        printf("&arr[%d]=%p\n",&arr[i]);
    }
    return 0;
}//得出的地址是连续开辟的空间，数组在内存中是连续存放的

//二维数组的创建
//int arr[3][4];
//char arr[3][5];
//double arr[2][4];

//二维数组的初始化
int mian()
{
    int arr[3][4]={1,2,3,4,5};//第一行1，2，3，4。第二行5，后面全补0
    int arr[3][4]={{1,2,3},{4,5}};//第一行1，2，3，0.第二行4，5，后面全补0
    //int arr[]={1,2,3,4};
    //int arr[][4]={{1,2,3,4},{5,6,7,8}};//行可以省略，列绝对不能省略
    return 0;
}

//二维数组的使用
int main()
{
    int arr[3][4]={1,2,3},{4,5}};
    int i=0;
    for(i=0;i<3;i++)
    {
        int j=0;
        for(j=0;j<4;j++)
        {
            printf("%d",arr[i][j]);
        }
        printf(\n");
    }
    return 0;
}

//二维数组在内存中的存储
int main()
{
    int arr[3][4]={1,2,3},{4,5}};
    int i=0;
    for(i=0;i<3;i++)
    {
        int j=0;
        for(j=0;j<4;j++)
        {
            printf("&arr[%d][%d]=%p",arr[i][j]);
        }
        printf(\n");
    }
    return 0;
}//和一维数组一样是连续存放的


