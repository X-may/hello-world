# hello-world
test
#include<iostream>
using namespace std;
class Goods
{
private:
	static int totalWeight;
	int weight;
public:
	Goods(int w){weight=w;totalWeight+=weight;cout<<"Create Goods"<<"\n";}
	int get(){return weight;}
	static int GetTotal(){return totalWeight;}
	~Goods(){cout<<"delete Goods"<<"\n";}
};
int Goods::totalWeight=0;
void main()
{
	Goods gs(20);
	cout<<gs.get()<<"/"<<gs.GetTotal()<<"\n";
	Goods gs2(23);
	cout<<gs2.get()<<"/"<<gs2.GetTotal()<<"\n";
}
