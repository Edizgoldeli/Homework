# Homework
Exam average calculator
#include <iostream>
#include <iomanip>
using namespace std;

int main()
{
    srand(time(0));
    const int grade = 100;
    const int grade2 = 100;
    
    int total=0;
    int total1=0;
    int ttl=0;
    int stdttl=0;
    int s[grade];
    int t[grade2];
    
    
    for(int i = 1 ;i<=grade ;i++)
    {  s[i]=rand()%100;
        t[i]=rand()%100;
        total += s[i];
        total1 += t[i];
        ttl= total*0.004+total1*0.006;
        
        
    }
    
    cout<<setw(7)<<"Student"<<setw(17)<<"Midterm(%40)"<<setw(17)<<"Final(%60)"<<setw(17)<<"Average"<<setw(20)<<"Status of Std.";
    
    for(int j=1;j<=grade;j++)
    {
        stdttl=s[j]*0.4+t[j]*0.6;
        
        cout<<"\n"<<setw(5)<<j<<setw(17)<<s[j]<<setw(17)<<t[j]<<setw(17)<<stdttl<<setw(17);
        
        if(stdttl<ttl)
        {
            cout<<setw(22)<<"UNDER";
        }
        if(stdttl==ttl)
        {
            cout<<setw(19)<<"EQUAL";
        }
        
        if(stdttl>ttl)
        {
            cout<<"ABOVE ";
        }
    }
    cout<<"\n\n";
    cout<<"Midterm Av."<<setw(17)<<"Final av."<<setw(17)<<"Total Av.\n";
    cout<<setw(10)<<total/100<<setw(17)<<total1/100<<setw(20)<<ttl<<"\n";
    
}
