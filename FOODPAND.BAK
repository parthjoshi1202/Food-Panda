#include<fstream.h>
#include<iomanip.h>
#include<graphics.h>
#include<stdlib.h>
#include<conio.h>
#include<stdio.h>
#include<string.h>
#include<dos.h>
void menu(char na[20],char co[]);
void bill(char na[],char co[]);
//char order[10][20];
int d=0,pr[10];
class orde
   {  public:
   char code[10];
   char customername[20];
   char item[20];
   int price;
   };
char north[20][20]={"Dal Fry ",
		    "Yellow Dal ",
		    "Karhi Pakora   ",
		    "Chana Masala   ",
		    "Rajma",
		    "Dal Makhani    ",
		    "Mix Vegetable  ",
		    "Palak Paneer   ",
		    "Palak Kofta    ",
		    "Matar Paneer   ",
		    "Malai Kofta    ",
		    "Shahi Paneer   ",
		    "Mushroom Masala",
		    "Karahi Paneer  ",
		    "Matar Mushroom ",
		    "Plain Roti     ",
		    "Butter Roti    ",
		    "Lachha Paratha ",
		    "Plain Naan     ",
		    "Butter Naan    ",
		    };

int nop[20]={150,140,180,170,200,180,160,180,170,180,160,170,200,160,160,20,30,40,40 ,
		     50 ,   };

char chinese[15][30]={"Cheese Manchurian",
		      "Veg Manchurian",
		      "Veg Noodles ",
		      "Spl Noodles",
		      "Veg Fried Rice",
		      "Honey Chilli Potatoes",
		      "Chilli Chaap",
		      "Chilli Mushroom" ,
		      "Veg Spring Roll",
		      "Veg Fried Momos",
		      "Veg Steam Momos",
		      "Paneer Fried Momos",
		      "Paneer Steam Momos",
		      "Chicken momos",

		      "Chicken roll",
					}   ;
int chp[15]={220,
			180,
			 150,
			  180,
			   170,
			   180,
			   200,
			   190,
			   150,
			   140,
			   120,
			   160,
			   150,
			   180,
			   200,
		      };

char sweet[10][30]={"Choco Lava",
		       "Rabri Faluda",
		       "Spl Kesar Matka Kulfi",
		       "GulabJamun",
		       "Rasmalai",
		       "Bengali Rasgulla",
		       "Sweet Lassi",
		       "Chocolate Ice-cream",
		       "Vanilla Ice-cream",
		       "Sunday Ice-cream",
		       }                     ;
int swp[10]={120,
			 150,
			    80,
			    60,
			   120,
		       150,
		       50,
		       150,
		       120,
		       200,};

char beverages[15][20]={"Bislery Water",
			   "Coke",
			   "Pepsi",
			   "Fanta",
			   "Limca",
			   "Sprite",
			   "Masala tea",
			   "Coffee",
			   "Oreo Shake",
			   "Stawberry Shake",
			   "Chocolate Shake",
			   "Mango Shake",
			   "Mixed Fruit Juice",
			   "Pineapple Juice",
			   "Viegin Mojito",
			   }                  ;
int bep[15]={30, 50,  50,  50, 50,50,40,60,80, 70, 80, 60,50, 60,100,};

void bill(char n[20],char co[10])
{
 cleardevice();

      setbkcolor(BLACK);
      setcolor(RED);   orde o;
      settextstyle(3,0,7);
      outtextxy(150,20,"FOOD PANDA") ;
      outtextxy(250,80,"BILL") ;

      settextstyle(3,0,6);
      setcolor(BLUE);
      settextstyle(3,0,3);
      outtextxy(50,160," Customer name");
      outtextxy(250,160,n);
      outtextxy(50,180," Bill code");
      outtextxy(250,180,co);

     // cout<<"\n\t Customer Name "<<n<<"         Bill Code     "<<co;
      fstream iof;
      iof.open("order.dat",ios::in|ios::app|ios::binary);
      gotoxy(20,13);
      cout<<"\n\n\t Particulars                 Price";
     //outtextxy(80,220,"Particulars                           Price");
      int sum=0;
      while(iof.read((char*)&o,sizeof(o)))
      {
       if(strcmp(o.code,co)==0)
	  {        //  gotoxy(20,15);
	  cout<<"\n"<<setw(20)<<o.item<<setw(20)<<o.price;
       //	 outtextxy(80,240,o.item);
	// outtextxy(180,240,o.price);
	  sum=sum+o.price;
	  }
	  }
cout<<"\n\n\n\n\t\t  Amount  "<<sum;

      getch();
  //    settextstyle(3,0,4);
    //  outtextxy(20,90,"INDIAN KITCHEN");
     // getch();
}

char *northmenu(char na[20],char co[])
	{ int k=0;
 fstream iof;
 iof.open("order.dat",ios::in|ios::app|ios::binary);
		  orde o;
 char c;
	int s=0;
	do
	{
	cleardevice();
	setcolor(RED);
	settextstyle(3,0,7);
	settextstyle(3,0,4);
	outtextxy(20,100,"NORTH INDIAN");
 int x=2,y=10;
 for(int i=0;i<20;i++)
	{
       gotoxy(x,y);
       cout<<i+1<<"."<<north[i]<<"  "<<nop[i];
       y++;
    if(y%10==0)
	 {
    y=10;x=x+25;
	 }
	 }
   int ch;
   cout<<"\nEnter ur Choice";
   cin>>ch;

   for(i=0;i<22;i++)
	{
		if(i==ch)
	{
	 cout<<"\n\n\t You have Selected ";
	 cout<<"\n\n\t"<<north[i-1]<<"  "<<nop[i-1];
	 strcpy(o.item,north[i-1]);
	 strcpy(o.customername,na);
	 strcpy(o.code,co);
	 o.price=nop[i-1];
	 iof.write((char*)&o,sizeof(o)); k++;
	 }
	 }
     cout<<"\n\n\t\tDo u want to enter more";
     cin>>c;                 }

 while((c=='y')||(c=='Y'));
   getch();
   cleardevice();
  return na;                }

char *chinesemenu(char na[20],char co[])

 { int k=0;   fstream iof;
	iof.open("order.dat",ios::in|ios::app|ios::binary);
	 orde o;
	 char c;
	 int s=0;
	do{

      cleardevice();
	setcolor(RED);
	settextstyle(3,0,7);
	settextstyle(3,0,4);
	outtextxy(20,100,"Chinese");
 int x=2,y=10;
 for(int i=0;i<15;i++)
    {  gotoxy(x,y);
       cout<<i+1<<"."<<chinese[i]<<"  "<<chp[i];
       y++;
    if(y%10==0)
    {y=10;x=x+25;}     }
      int ch;
      gotoxy(20,19);
    cout<<"\n\nEnter ur Choice";
    cin>>ch;
    for( i=0;i<20;i++)
	{ if(i==ch)
	{ cout<<"\n\n\t\t You have Selected ";
	 cout<<"\n\n\n\t"<<chinese[i-1]<<"  "<<chp[i-1];
	 strcpy(o.item,chinese[i-1]);
	 strcpy(o.customername,na);
	 o.price=chp[i-1];
	 strcpy(o.code,co);
	 k++;iof.write((char*)&o,sizeof(o));
	 }
	 }
     cout<<"\n\n\t\tDo u want to enter more";
     cin>>c;                 }

 while((c=='y')||(c=='Y'));
   getch();
   cleardevice();
       return na;
	 }


char *sweetmenu(char na[20],char co[])

      {    fstream iof;     int k=0;
	iof.open("order.dat",ios::in|ios::app|ios::binary);
 orde o;
 char c;
 int s=0;
do{

     cleardevice();
	setcolor(RED);
	settextstyle(3,0,7);
	settextstyle(3,0,4);
	outtextxy(20,100,"Sweet Dish");
	 int x=2,y=10;
	 for(int i=0;i<10;i++)
    {  gotoxy(x,y);
       cout<<i+1<<"."<<sweet[i]<<"  "<<swp[i];
       y++;
    if(y%10==0)
    {y=10;x=x+25;}
  }
     int ch;
    cout<<"\n\nEnter ur Choice";
    cin>>ch;
    for( i=0;i<20;i++)
	{ if(i==ch)
	{ cout<<"\n\n\t\t You have Selected ";
	 cout<<"\n\n\n\t"<<sweet[i-1]<<"  "<<swp[i-1];
		 strcpy(o.item,sweet[i-1]);
	 strcpy(o.customername,na);
	 o.price=swp[i-1];
	 strcpy(o.code,co);
	 iof.write((char*)&o,sizeof(o)); k++;
	 }
	 }
     cout<<"\n\n\t\tDo u want to enter more";
     cin>>c;                 }

 while((c=='y')||(c=='Y'));
   getch();
   cleardevice();

	 }
char *beveragesmenu(char na[20],char co[])

 {        fstream iof;
	iof.open("order.dat",ios::in|ios::app|ios::binary);
orde o;int k=0;
 char c;
 int s=0;
do{

     cleardevice();

	setcolor(RED);
	settextstyle(3,0,7);
	settextstyle(3,0,4);
	outtextxy(20,100,"Beverages");
 int x=2,y=10;
 for(int i=0;i<15;i++)
    {  gotoxy(x,y);
       cout<<i+1<<"."<<beverages[i]<<"  "<<bep[i];
       y++;
    if(y%10==0)
    {y=10;x=x+25;}  }
    int ch;
     gotoxy(20,19);
     cout<<"\n\nEnter ur Choice";
    cin>>ch;
    for( i=0;i<20;i++)
	{ if(i==ch)
	{ cout<<"\n\n\t\t You have Selected ";
	 cout<<"\n\n\n\t"<<beverages[i-1]<<"  "<<bep[i-1];
	 strcpy(o.item,beverages[i-1]);
	 strcpy(o.customername,na);
	 o.price=bep[i-1];
	 strcpy(o.code,co);
	 iof.write((char*)&o,sizeof(o)); k++;
	 }
	 }
     cout<<"\n\n\t\tDo u want to enter more";
     cin>>c;                 }

 while((c=='y')||(c=='Y'));
   getch();
   cleardevice();
      return na;
	 }
 void abc()
     {      //exit(0);

     cleardevice();
     getch();
      }
 void main()

{
 int gdriver = DETECT, gmode, errorcode;
 initgraph(&gdriver, &gmode, "c:\\turboc3\\bgi");
 setbkcolor(BLACK);    int x,y,i;
 x=getmaxx()/3.5;
 y=getmaxy()/3.5;
 for( i=40;i<200;i++)
	 {
 delay(10);
 setcolor(i/10);
 arc(x,y,0,360,i-10);
	 }
 x=getmaxx()/1.1;
 y=getmaxy()/1.1;
 for( i=40;i<120;i++)
	{
 delay(10);
 setcolor(i/10);
 arc(x,y,0,360,i-10);
	}
 setcolor(BLUE);
 setcolor(WHITE);
 settextstyle(1,0,7);
 outtextxy(40,340,"FOOD PANDA");
 delay(20);

 getch();
	char na[15];
	char phno[12];
	char restaurant[20];
	char address[20],co[10];
cleardevice();
	setbkcolor(BLUE);
	setcolor(WHITE);
	settextstyle(1,0,7);
	for( i=0;i<300;i++)
	{ cleardevice();
	outtextxy(i+150,50,"FOOD PANDA"); delay(5);
	if (i==299)
       {cleardevice();	outtextxy(150,50,"FOOD PANDA");} }
	setcolor(WHITE);
	settextstyle(3,0,2);
	rectangle(10,30,580,120);
	rectangle(18,200,600,450);
	outtextxy(20,200,"ENTER YOUR NAME:");
	gotoxy(28,14);
	gets(na);
	outtextxy(20,230,"ENTER YOUR PHONE NUMBER:");
	gotoxy(40,16);
	cin>>phno;
	check:
	outtextxy(20,260,"ENTER CODE:");
	gotoxy(46,18);
	cin>>co;           orde o;
	fstream iof;
	iof.open("order.dat",ios::in|ios::app|ios::binary);
	while(!iof.eof())
	{
	iof.read((char*)&o,sizeof(o));
	if(strcmp(o.code,co)==0)
	  {
	     cout<<"\n code already exist";
	     goto check;
	     }}
	outtextxy(20,290,"DELIVERY LOCATION:");
	gotoxy(30,20);
	cin>>address;

	getch();
	char username[20];
	char password[15];
	cleardevice();
	setbkcolor(RED);
	setcolor(WHITE);
	settextstyle(3,0,4);
	outtextxy(236,10,"LOG IN...");
	outtextxy(175,110,"USERNAME:");
	rectangle(400,110,600,150);
	gotoxy(55,9);
	gets(username);
	outtextxy(185,190,"PASSWORD:");
	rectangle(400,200,600,240);
	gotoxy(55,15);
	cin>>password;
	getch();
	cleardevice();
	setbkcolor(GREEN);
	setcolor(1);
	x=getmaxx()/3.5;
 y=getmaxy()/3.5;
 for( i=40;i<135;i++)
	 {
 delay(10);
 setcolor(i/1);
 arc(x,y,0,180,i-1);
	 }
 x=getmaxx()/1.1;
 y=getmaxy()/1.1;
 for( i=40;i<0;i++)
	{
 delay(10);
 setcolor(i/1);
 arc(x,2,0,180,i-1);

	}

       //	outtextxy(20,310,"DESSERTS");

       //	outtextxy(20,340,"BEVERAGES");

getch();
   int ch;
   do{
   setcolor(RED);             char c[20];
	settextstyle(3,0,7);
	outtextxy(20,130,"TYPES OF FOOD");
	settextstyle(3,0,4);
	outtextxy(20,220,"1.NORTH INDIAN");

	outtextxy(20,250,"2.CHINESE");

	outtextxy(20,280,"3.SWEET DISH");
	outtextxy(20,310,"4.BEVERAGES");
	outtextxy(540,440,"5.BILL");
	rectangle(350,360,450,394);
	outtextxy(20,360,"ENTER YOUR CHOICE");
	gotoxy(47,24);
	cin>>ch;
	switch(ch)
	{
	case 1:
	strcpy(c,northmenu(na,co));break;
	case 2:
	strcpy(c,chinesemenu(na,co));break;
	case 3:
	strcpy(c,sweetmenu(na,co));break;
	case 4:
	strcpy(c,beveragesmenu(na,co));break;
	case 5:
	bill(c,co);break;
	 }
	 }
	 while(ch!=5);
   }

