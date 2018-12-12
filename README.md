###### Fn99
    #include <stdio.h>
    #include <stdlib.h>
    #include <string.h>
    #include <math.h>
    #include<windows.h>
    #include <conio.h>


    struct Student
    {    char xuehao[1000];
         char xingbie[1000];
         char xingming[1000];
         char banji[1000];
         char dianhua[1000];
         char chusheng[1000];};
    struct Student students[1000];

    int num=0;
    int main()
    {
        void shuru();
        void xianshi();
        void chazhao();
        void zengjia();
        void shanchu();
        void tuichu();
        void xiugai();
        int y;
        while(1){
        system("cls");
        printf("————————学—生—学—籍—管—理—系—统————————");
        printf("\n");
        printf("\n");
        printf("  请    选     择     功     能\n");
        printf("(1)输入数据\n");
        printf("\n");
        printf("(2)显示数据\n");
        printf("\n");
        printf("(3)查找数据\n");
        printf("\n");
        printf("(4)增加一条数据\n");
        printf("\n");
        printf("(5)删除一条数据\n");
        printf("\n");
        printf("(6)修改一条数据\n");
        printf("\n");
        printf("(7)退出\n");
        printf("\n");
        printf("输入您的选择 1~7\n");
        printf("\n");
        scanf("%d",&y);
        getchar();
        switch(y){case 1:shuru();break;
                  case 2:xianshi();break;
                  case 3:chazhao();break;
                  case 4:zengjia();break;
                  case 6:xiugai();break;
                  case 5:shanchu();break;
                  case 7:exit(0);break;
                  }}}
        void shuru(){
            char x[100];char z;int m1,m2,m3,m4,m5,m6;m1=m2=m3=m4=m5=m6=1;
        system("cls");
        printf("一. 输入数据 \n");
        while(1){while(m1==1){
        printf("请输入您的学号\n");
        scanf("%s",&students[num].xuehao);
        system("cls");
        printf("您的学号是\n");
        printf("%s\n",students[num].xuehao);
        printf("请仔细核对，需要重新输入，输入Y\n");
        printf("            不需要重新输入，输入任意\n");
        scanf(" %c",&z);
        system("cls");
        if(z!='Y')m1=0;}
        while(m2==1){
        printf("请输入您的姓名\n");
        scanf("%s",&students[num].xingming);
        system("cls");
        printf("您的姓名是\n");
        printf("%s\n",students[num].xingming);
        printf("请仔细核对，需要重新输入，输入Y\n");
        printf("            不需要重新输入，输入任意\n");
        scanf(" %c",&z);
        system("cls");
        if(z!='Y')m2=0;}
        while(m3==1){
        printf("请输入您的性别\n");
        scanf("%s",&students[num].xingbie);
        system("cls");
        printf("您的性别是\n");
        printf("%s\n",students[num].xingbie);
        printf("请仔细核对，需要重新输入，输入Y\n");
        printf("            不需要重新输入，输入任意\n");
        scanf(" %c",&z);
        system("cls");
        if(z!='Y')m3=0;}
        while(m4==1){
        printf("请输入您的出生日期\n");
        scanf("%s",&students[num].chusheng);
        system("cls");
        printf("您的出生日期是\n");
        printf("%s\n",students[num].chusheng);
        printf("请仔细核对，需要重新输入，输入Y\n");
        printf("            不需要重新输入，输入任意\n");
        scanf(" %c",&z);
        system("cls");
        if(z!='Y')m4=0;}
        while(m5==1){
        printf("请输入您的所在班级\n");
        scanf("%s",&students[num].banji);
        system("cls");
        printf("您的所在班级是\n");
        printf("%s\n",students[num].banji);
        printf("请仔细核对，需要重新输入，输入Y\n");
        printf("            不需要重新输入，输入任意\n");
        scanf(" %c",&z);
        system("cls");
        if(z!='Y')m5=0;}
        while(m6==1){
        printf("请输入您的联系方式\n");
        scanf("%s",&students[num].dianhua);
        system("cls");
        printf("您的联系方式是\n");
        printf("%s\n",students[num].dianhua);
        printf("请仔细核对，需要重新输入，输入Y\n");
        printf("            不需要重新输入，输入任意\n");
        scanf(" %c",&z);
        system("cls");
        if(z!='Y')m6=0;}
        printf("输入完成\n");
        num++;
        printf("输入下一组新数据，输入Y\n");
        printf("返回主菜单，输入F\n");
        scanf(" %c",&z);getchar();
        if(z=='Y')m1=m2=m3=m4=m5=m6=1;system("cls");
        if(z=='F')break;system("cls");
        }}
        void xianshi()
    {    int i;
          system("cls");
          printf("%15s%15s%15s%15s%15s%15s\n","学号","所在班级","姓名","性别","生日","联系方式");
               for (i=0;i<num;i++){printf("%15s%15s%15s%15s%15s%15s\n",students[i].xuehao,students[i].banji,students[i].xingming,students[i].xingbie,students[i].chusheng,students[i].dianhua);}
            printf("            输入任意键继续      \n");
            getchar();
            }

        int idfanhui(char id[])

    {
         int i;
         for (i=0;i<num;i++)
         {
             if (strcmp(students[i].xuehao,id)==0)
            {

                 return i;

             }

         }

         return -1;

    }

    int xingmingfanhu(char name[])

    {

         int i;

         for (i=0;i<num;i++)

         {

             if (strcmp(students[i].xingming,name)==0)

             {

                  return i;

             }

         }

         return -1;

    }


    void xiugai()

    {


         while(1)

         {

             char id[20];

             int HHH;
             system("cls");
             printf("————————学—生—学—籍—管—理—系—统————————");
             printf("\n");
             printf("\n");
             printf("请输入要改动的学生的学号:");

             scanf("%s",&id);

             getchar();

             HHH=idfanhui(id);

             if (HHH==-1)

             {

                  printf("学生不存在!\n");

             }

             else

             {

                  printf("你要改动的学生信息为:\n");

                  xianshi(HHH);
                  printf("\n");
                  printf("-- 请输入新数据--\n");
                  printf("请输入学号:");
                  scanf("%s",&students[HHH].xuehao);
                  getchar();
                  printf("请输入班级:");
                  scanf("%s",&students[HHH].banji);
                  getchar();
                  printf("请输入姓名:");
                  scanf("%s",&students[HHH].xingming);
                  getchar();
                  printf("请输入性别:");
                  scanf("%s",&students[HHH].xingbie);
                  getchar();
                  printf("请输入出生日期:");
                  scanf("%s",&students[HHH].chusheng);
                  getchar();
                  printf("请输入联系方式:");
                  scanf("%s",&students[HHH].dianhua);
                  getchar();



             }

             printf("是否继续?      (任意键继续/n)  \n");

             if (getchar()=='n')

             {

                  break;

             }

         }

    }


    void shanchu()

    {

         int i;

         while(1)

         {

             char id[20];

             int LLL;
             system("cls");
             printf("————————学—生—学—籍—管—理—系—统————————");
             printf("\n");
             printf("\n");
             xianshi();
             printf("请输入要删除的学生的学号:");
             printf("\n");
             scanf("%s",&id);

             getchar();

             LLL=idfanhui(id);

             if (LLL==-1)

             {

                  printf("学生不存在!\n");

             }

             else

             {

                  printf("你要删除的学生信息为:\n");

                  printf("\n");
            printf("%15s%15s%15s%15s%15s%15s\n","学号","所在班级","姓名","性别","生日","联系方式");
    printf("%15s%15s%15s%15s%15s%15s\n",students[LLL].xuehao,students[LLL].banji,students[LLL].xingming,students[LLL].xingbie,students[LLL].chusheng,students[LLL].dianhua);

                  printf("是否真的要删除?(y/任意键继续)\n");
                  printf("\n");
                  if (getchar()=='y')

                  {

                       for (i=LLL;i<num-1;i++)

                       {

                           students[i]=students[i+1];//把后边的对象都向前移动

                       }

                       num--;

                  }

                  getchar();printf("删除成功\n");

             }

              printf("\n");
             printf("是否继续?(任意键继续/n)\n");
              printf("\n");
             if (getchar()=='n')

             {

                  break;

             }

         }

    }

    void chazhao()
    {

         while(1)

         {

             char name[20];

             int XXX,a;

            system("cls");
             printf("————————学—生—学—籍—管—理—系—统————————");
             printf("\n");
             printf("\n");
             printf("请选择查询方式\n");
             printf("1.  学号\n");
             printf("\n");
             printf("2.  姓名\n");
             printf("\n");

             printf("\n");
             printf("请输入数字 ：   \n");
             scanf("%d",&a);

             getchar(); system("cls");printf("————————学—生—学—籍—管—理—系—统————————");
             printf("\n");
             printf("\n");
            if(a==1)
            {
                    printf("请输入要查询的学生的学号:\n");
             scanf("%s",&name);
             XXX=idfanhui(name);
            if (XXX==-1)
            {printf("学生不存在!\n"); printf("\n");}
            else
           {printf("你要查询的学生信息为:\n");
           printf("\n");
            printf("%15s%15s%15s%15s%15s%15s\n","学号","所在班级","姓名","性别","生日","联系方式");
    printf("%15s%15s%15s%15s%15s%15s\n",students[XXX].xuehao,students[XXX].banji,students[XXX].xingming,students[XXX].xingbie,students[XXX].chusheng,students[XXX].dianhua);
              }

             printf("\n");printf("是否返回?(任意键继续/n)\n");
             getchar();
             if (getchar()!='n')

             {

                  break;system("cls");

             }

            }
            if(a==2){
                    printf("请输入要查询的学生的姓名:\n");
             scanf("%s",&name);
             XXX=xingmingfanhu(name);
            if (XXX==-1)
            {printf("学生不存在!\n");printf("\n"); }
            else
           {printf("你要查询的学生信息为:\n");
           printf("\n");
            printf("%15s%15s%15s%15s%15s%15s\n","学号","所在班级","姓名","性别","生日","联系方式");
    printf("%15s%15s%15s%15s%15s%15s\n",students[XXX].xuehao,students[XXX].banji,students[XXX].xingming,students[XXX].xingbie,students[XXX].chusheng,students[XXX].dianhua);
              }

             printf("\n");printf("是否返回?(任意键返回/n)\n");getchar();

             if (getchar()!='n')

             {

                  break;

             }

         }

         }

    }

    void zengjia(){system("cls"); printf("————————学—生—学—籍—管—理—系—统————————");
             printf("\n");
             printf("\n");while(1){
     printf("-- 请输入新数据--\n");
                  printf("请输入学号:");
                  scanf("%s",&students[num].xuehao);
                  getchar();
                  printf("请输入班级:");
                  scanf("%s",&students[num].banji);
                  getchar();
                  printf("请输入姓名:");
                  scanf("%s",&students[num].xingming);
                  getchar();
                  printf("请输入性别:");
                  scanf("%s",&students[num].xingbie);
                  getchar();
                  printf("请输入出生日期:");
                  scanf("%s",&students[num].chusheng);
                  getchar();
                  printf("请输入联系方式:");
                  scanf("%s",&students[num].dianhua);
                  getchar();
                  num++;
                  printf("\n");printf("是否返回?(任意键继续/n)\n");getchar();

             if (getchar()!='n')

             {

                  break;

             }}







    }
