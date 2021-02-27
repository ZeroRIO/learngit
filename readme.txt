#include <cstdlib>
#include <iostream>
#include <ctime>
using namespace std;

int main()
{
    int num1,num2,op,result1,result2,m,n,i;

    srand(time(NULL));
for(i=0;i<3;++i)
    {
    m=rand()%10;
    n=rand()%10;
    num1=max(m,n);
    num2=min(m,n);
    op=rand()%4;

    switch(op){
        case 0:cout<<num1<<"+"<<num2<<"=?"<<endl;
        cin>>result1;
        if(num1+num2==result1) cout<<"right\n";
        else cout<<"wrong\n";
        break;

        case 1:cout<<num1<<"-"<<num2<<"=?"<<endl;
        cin>>result1;
        if(num1-num2==result1) cout<<"right\n";
        else cout<<"wrong\n";
        break;

        case 2:cout<<num1<<"*"<<num2<<"=?"<<endl;
        cin>>result1;
        if(num1*num2==result1) cout<<"right\n";
        else cout<<"wrong\n";
        break;

        case 3:cout<<num1<<"/"<<(num2!=0?num2:num2+1)<<"=?"<<endl;
        cin>>result1;
        cout<<"余数为:?"<<endl;
        cin>>result2;
        if((num1/num2==result1)&&(num1%num2==result2)) cout<<"right\n";
        else cout<<"wrong\n";
        break;
        }
    }
    return 0;
}
