#include<iostream.h>
#include<conio.h>
#include<stdlib.h>
int a[9]={1,2,3,4,5,6,7,8,9};
int win_a=0;
int win_b=0;
int w_a=0;
int w_b=0;
void design(int d);
void checking(int *no_one,int *play);
void double_entry(int d_a[9],int *n,int *s,int *p);
void show(int n,int *p);
void main()
{
	int starter,player=1,pos,re_start;
	int no_one=0,play=0,d_a[9]={0},d_s=0,d_c=0;
	clrscr();
	top:
	cout<<"\npress 1 for start the game\npress 2 for exit the game\n";
	choice:
	cout<<"your choice:- ";
	cin>>starter;
	switch(starter)
	{
		case 1:
		{
			goto start_game;
		}
		case 2:
		{
			goto exit_game;
		}
		default:
		{
			cout<<"\nwrong entry\nre-enter ";
			goto choice;
		}
	}
	// for exit the game
	exit_game:
	{
		exit(0);
	}
	 //now start the game
	start_game:
	       clrscr();
	       design(d_c);
	       d_c=0;
	//for player chance
	if(player%2==1&&player<10&&play==0)
	{
		//design for A player
		cout<<"\nplayer A chance";
		cout<<"\nenter the position:- ";
		cin>>pos;
		d_a[d_s]=pos;
		double_entry(d_a,&d_c,&d_s,&pos);
		if(d_c==0)
		{
			++d_s;
			player++;
			a[pos-1]=11;
			no_one=0;
			checking(&no_one,&play);
		}
		goto start_game;
	}
	else if(player%2==0&&player<10&&play==0)
	{
		//design for B player
		cout<<"\nplayer B chance";
		cout<<"\nenter the position:- ";
		cin>>pos;
		d_a[d_s]=pos;
		double_entry(d_a,&d_c,&d_s,&pos);
		if(d_c==0)
		{
			++d_s;
			player++;
			a[pos-1]=12;
			no_one=0;
			checking(&no_one,&play);
		}
		goto start_game;
	}
	//for restart the game
	if(no_one==1)
	{
		cout<<"\nNo one is win";
		no_one=0;
	}
	cout<<"\n\ndo you want to restart the game?";
	cout<<"\npress 1 for start a new game\npress any key to exit";
	cin>>re_start;
	switch(re_start)
	{
		case 1:
		{
			player=1;no_one=0;play=0;
			for(d_s=0;d_s<9;d_s++)
			{
				a[d_s]=d_s+1;
				d_a[d_s]=0;
			}
			d_s=0;w_a=0;w_b=0;
			goto start_game;
		}
		default:
		{
			exit(0);
		}
	}
	getch();
}
void design(int d)
{
	//design of game
	cout<<"start game-\n";
	cout<<"\n     |     |      \t\t _ _ _ _ _ _ _ _ ";
	cout<<"\n  ";
	if(a[0]==1)
		cout<<a[0];
	else if(a[0]==11)
		 cout<<"o";
	else
		cout<<"x";
	cout<<"  |  ";
	if(a[1]==2)
		cout<<a[1];
	else if(a[1]==11)
		cout<<"o";
	else
		cout<<"x";
	cout<<"  |  ";
	if(a[2]==3)
		cout<<a[2];
	else if(a[2]==11)
		cout<<"o";
	else
		cout<<"x";
	cout<<"  \t\t| _ _winning_ _ |";
	cout<<"\n_ _ _|_ _ _|_ _ _\t\t|_ _A_ _|_ _B_ _|";
	cout<<"\n     |     |     \t\t|       |       |";
	cout<<"\n  ";
	if(a[3]==4)
		cout<<a[3];
	else if(a[3]==11)
		cout<<"o";
	else
		cout<<"x";
	cout<<"  |  ";
	if(a[4]==5)
		cout<<a[4];
	else if(a[4]==11)
		cout<<"o";
	else
		cout<<"x";
	cout<<"  |  ";
	if(a[5]==6)
		cout<<a[5];
	else if(a[5]==11)
		cout<<"o";
	else
		cout<<"x";
	cout<<"   \t\t|   "<<win_a<<"   |   "<<win_b<<"   |";
	cout<<"\n_ _ _|_ _ _|_ _ _\t\t|_ _ _ _|_ _ _ _|";
	cout<<"\n     |     |     ";
	cout<<"\n  ";
	if(a[6]==7)
		cout<<a[6];
	else if(a[6]==11)
		cout<<"o";
	else
		cout<<"x";
	cout<<"  |  ";
	if(a[7]==8)
		cout<<a[7];
	else if(a[7]==11)
		cout<<"o";
	else
		cout<<"x";
	cout<<"  |  ";
	if(a[8]==9)
		cout<<a[8];
	else if(a[8]==11)
		cout<<"o";
	else
		cout<<"x";
	cout<<"  \t\t";
	if(w_a==1)
	{
		cout<<"player A is win!";
	}
	if(w_b==1)
	{
		cout<<"player B is win!";
	}
	if(d==1)
	{
		cout<<"Already entered position";
	}
	cout<<"\n     |     |     ";
	//end of design
}
void double_entry(int d_a[9],int *c,int *s,int *p)
{
	int i;
	for(i=0;i<*s;i++)
	{
		if(d_a[i]==*p)
		{
			++*c;
		}
	}
}
void checking(int *no_one,int *play)
{
	//for check the all condition of game
	if(a[0]==a[1]&&a[1]==a[2])
	{
		show(0,&*play);
	}
	else if(a[3]==a[4]&&a[4]==a[5])
	{
		show(3,&*play);
	}
	else if(a[6]==a[7]&&a[7]==a[8])
	{
		show(6,&*play);
	}
	else if(a[0]==a[3]&&a[3]==a[6])
	{
		show(0,&*play);
	}
	else if(a[1]==a[4]&&a[4]==a[7])
	{
		show(1,&*play);
	}
	else if(a[2]==a[5]&&a[5]==a[8])
	{
		show(2,&*play);
	}
	else if(a[0]==a[4]&&a[4]==a[8])
	{
		show(0,&*play);
	}
	else if(a[2]==a[4]&&a[4]==a[6])
	{
		show(2,&*play);
	}
	else
	{
		++*no_one;
	}
	//end of check condition
}
//for checking and increment win of the game
void show(int n,int *p)
{
	if(a[n]==11)
	{
		++win_a;
		++w_a;
		++*p;
	}
	else
	{
		++win_b;
		++w_b;
		++*p;
	}
}
//end...
