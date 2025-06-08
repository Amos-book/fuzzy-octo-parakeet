# fuzzy-octo-parakeet
#include <iostream>
#include<string.h>
using namespace std;
class Pet//宠物类
  {private:
      char name[10];//宠物名
      char  song[10];//应答语
   public:
     Pet(char *na,char *s)//初始化
    {strcpy(name,na); strcpy(song,s);}
   void  answer(char *message)//应答
    { if(!strcmp(message,name))
     { cout<<"I am  "<<name<<endl;
      cout<<song<<endl;
     }
     else
     cout<<"dear host,you are not calling me! "<<endl;
    }
 } ;

class  Host//主人类
{private:
     char name[10];
 public:
     Host(char *na){strcpy(name,na);}
     void call(Pet p,char *mes)//召唤宠物
     {p.answer(mes);}
};

int main()
{Host  Li("Lixue");
 Pet dog("smallflower", "wangwang");
 Pet cat("bigflower", "miaomiao");
 Li.call(dog, "smallflower");
 Li.call(cat, "bigflower");
 return 0;
}


