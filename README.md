#include<iostream>
#include<ctime>
#include<cstdlib>
using namespace std;
int main()
{
	int gnum;
	int turns=20;
	srand(time(0));
	int radnum=rand()%100+1;
	cout<<"**********************WELCOME TO THE NUMBER GUESSING GAME****************************"<<endl;
	cout<<"GUESS THE NUMBER BETWEEN 1 TO 100"<<endl;
	cout<<"TOTAL NUMBER OF TURN : 20"<<endl;
	do
	{
		cout<<"Enter your guessing number:";
		cin>>gnum;
		turns--;
		if(gnum>radnum)
        {
        	cout<<"Your guess is high!! Try again!"<<endl;
        	cout<<"Number of turns left:"<<turns<<endl;
		}
		else if(gnum<radnum)
		{
			cout<<"Your guess is low!! Try again!"<<endl;
		    cout<<"Number of turns left:"<<turns<<endl;
		}
		else
		{
			cout<<"Congragulation !!!! you guessed the correct number!"<<endl;
		}		
	}while(gnum!=radnum);
	return 0;
	
}
