#include<stdio.h>
#include<conio.h>
void main()
{
char a,order,b;
int n,i,item[20],x[20],bill=0,sum,price=0,i1=1,ad=0,c;
clrscr();
printf("\t\t\t********WELCOME********");
printf("\n\t\t\t\t   To");
printf("\n \t\t\t    Rosemary Kitchen\n");
printf("_______________________________________________________________________________");
printf("\n\n\n\n\n\n\n\n\n\t\t\tPlease Enter to continue");
getchar();
clrscr();
printf("\n\n\n\n\n\n\n\n\n\n\t\t\t\tAre you a VEGAN ?");
printf("\n\t\t\t      IF YES PRESS Y ELSE N\n ");
printf("\t\t\t\t\t");
scanf("%c",&a);
clrscr();
printf("\n\t\t\t\tROSEMARY KITCHEN\n");
printf("________________________________________________________________________________");
if(a=='y'|| a=='Y')
	{
	 printf("\n\n\t\t\t\t    VEG MENU");
	 printf("\n\t\t\t\t________________");
	 printf("\n ----------------------------------------------------------------------------\n");
	 printf("|\t<_STARTER_>\t\t\t|11.Coconut And\t\t\t     |");
	 printf("\n|1.Sweet Potato\t\t\t\t|   Corn Curry.....................$2|\n");
	 printf("|  Tikki.....................$3\t\t|12.Baked Vegan\t\t\t     |\n");
	 printf("|2.Smoky Vegan\t\t\t\t|   Korma..........................$3|\n");
	 printf("|  Mushroom..................$2\t\t|13.Butternut,Chestnut\t\t     |\n");
	 printf("|3.Roasted Harissa\t\t\t|   & Lential Cake.................$6|\n");
	 printf("|  Cauliflower...............$3\t\t|\t  <_Drinks & Beverage_>      |\n");
	 printf("|4.Carrot soup...............$5\t\t|14.Tea............................$1|\n");
	 printf("|\t<_MAIN COURSE_>\t\t\t|15.Americano......................$2|\n");
	 printf("|5.Salt & Pepper Tofu........$7\t\t|16.Boba...........................$2|\n");
	 printf("|6.Vegan Biryani.............$4\t\t|17.Milkshake......................$1|\n");
	 printf("|7.Beetroot and Onion          \t\t|18.Pepsi..........................$2|\n");
	 printf("|  Tarte.....................$4\t\t|19.Coca Cola......................$1|\n");
	 printf("|8.Vegan Meatballs...........$3\t\t|\t    <_Desserts_>\t     |\n");
	 printf("|9.Stuffed Coriander\t\t\t|20.Trifle.........................$2|\n");
	 printf("|  Pumkin....................$4\t\t|21.Ice Cream......................$1|\n");
	 printf("|10.Corn & Split\t\t\t|22.Macaroons......................$2|\n");
	 printf("|  Pea Chowder...............$3\t\t|23.Muffin.........................$1|\n");
	 printf(" ----------------------------------------------------------------------------\n");
	 printf("Enter the number of item\n");
	 scanf("%d",&n);
	for(i=1;i<=n;i++)
		{
		printf("Enter the serial no. of item you want to order\n");
		scanf("%d",&item[i]);
		printf("Number of servings\n");
		scanf("%d",&x[i]);
		}
printf("Do you want to add any more item enter y for yes and n for no\n");
getchar();
scanf("%c",&b);
if(b=='y' || b=='Y')
	{
	printf("Enter the number of item you want to add\n");
	scanf("%d",&ad);
	ad=ad+n;
		for(i=n+1;i<=ad;i++)
		{
		printf("Enter the serial no. of item\n");
		scanf("%d",&item[i]);
		printf("Enter the no. of servings\n");
		scanf("%d",&x[i]);
		}
	n=ad;
	}

	clrscr();
printf("\n*Press 1 to get You bill\n");
printf("*Press 2 to cancel the order\n");
scanf("%d",&b);
if(b==1)
	{
	goto cc;
	}
if(b==2)
	{
	goto bb;
	}



	cc:
	getchar();
	clrscr();
	printf("\t____________________________________________________________\n");
	printf("\t************************************************************\n");
	printf("\t                           Recepit                   \n");
	printf("\t************************************************************\n");
	printf("\t____________________________________________________________\n");
	printf("\tITEMS                     \t\tQty \tPRICE\n");
		for(i=1;i<=n;i++)
			{
					switch(item[i])
					{
					case 1:
					printf("\t%d.Sweet Potato\t\t\t\t%d\t$3\n",i1,x[i]);
					printf("\t  Tikki\n");
					price=3*x[i];
					bill=bill+price;
					i1++;
					break;
					case 2:
					printf("\t%d.Smoky Vegan\t\t\t\t%d\t$2\n",i1,x[i]);
					printf("\t   Mushroom\n");
					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 3:
					printf("\t%d.Roasted Harissa\t\t\t%d\t$3\n",i1,x[i]);
					printf("\t  Cauliflower\n");
					price=3*x[i];
					bill=bill+price;
					i1++;
					break;
					case 4:
					printf("\t%d.Carrot Soup\t\t\t\t%d\t$5\n",i1,x[i]);

					price=5*x[i];
					bill=bill+price;
					i1++;
					break;
					case 5:
					printf("\t%d.Salt & Pepper\t\t\t\t%d\t$7\n",i1,x[i]);
					printf("\t  Tofu\n");
					price=7*x[i];
					bill=bill+price;
					i1++;
					break;
					case 6:
					printf("\t%d.Vegan Biryani\t\t\t\t%d\t$4\n",i1,x[i]);

					price=4*x[i];
					bill=bill+price;
					i1++;
					break;
					case 7:
					printf("\t%d.Beetroot & Onion\t\t\t%d\t$4\n",i1,x[i]);
					printf("\t  Tarte\n");
					price=4*x[i];
					bill=bill+price;
					i1++;
					break;
					case 8:
					printf("\t%d.Vegan meatballs\t\t\t%d\t$3\n",i1,x[i]);

					price=3*x[i];
					bill=bill+price;
					i1++;
					break;
					case 9:
					printf("\t%d.Stuffed Coriander\t\t\t%d\t$4\n",i1,x[i]);
					printf("\t  Pumkin\n");
					price=4*x[i];
					bill=bill+price;
					i1++;
					break;
					case 10:
					printf("\t%d.Corn & Split\t\t\t\t%d\t$3\n",i1,x[i]);
					printf("\t  Pea Chowder\n");
					price=3*x[i];
					bill=bill+price;
					i1++;
					break;
					case 11:
					printf("\t%d.Cocunut &\t\t\t\t%d\t$2\n",i1,x[i]);
					printf("\t  Corn Curry\n");
					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 12:
					printf("\t%d.Baked Vegan\t\t\t\t%d\t$3\n",i1,x[i]);
					printf("\t  Korma\n");
					price=3*x[i];
					bill=bill+price;
					i1++;
					break;
					case 13:
					printf("\t%d.Butternut,Chestnut\t\t\t%d\t$6\n",i1,x[i]);
					printf("\t  And Lential Cake\n");
					price=6*x[i];
					bill=bill+price;
					i1++;
					break;
					case 14:
					printf("\t%d.Tea\t\t\t\t\t%d\t$1\n",i1,x[i]);

					price=1*x[i];
					bill=bill+price;
					i1++;
					break;
					case 15:
					printf("\t%d.Americano\t\t\t\t%d\t$2\n",i1,x[i]);

					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 16:
					printf("\t%d.Boba\t\t\t\t\t%d\t$2\n",i1,x[i]);

					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 17:
					printf("\t%d.Milkshake\t\t\t\t%d\t$1\n",i1,x[i]);

					price=1*x[i];
					bill=bill+price;
					i1++;
					break;
					case 18:
					printf("\t%d.Pepsi\t\t\t\t\t%d\t$2\n",i1,x[i]);

					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 19:
					printf("\t%d.Coca Cola\t\t\t\t%d\t$1\n",i1,x[i]);

					price=1*x[i];
					bill=bill+price;
					i1++;
					break;
					case 20:
					printf("\t%d.Trifle\t\t\t\t%d\t$2\n",i1,x[i]);

					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 21:
					printf("\t%d.Ice Cream\t\t\t\t%d\t$1\n",i1,x[i]);

					price=1*x[i];
					bill=bill+price;
					i1++;
					break;
					case 23:
					printf("\t%d.Muffin\t\t\t\t%d\t$1\n",i1,x[i]);

					price=1*x[i];
					bill=bill+price;
					i1++;
					break;
					case 22:
					printf("\t%d.Macaroons\t\t\t\t%d\t$2\n",i1,x[i]);

					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					default:
					printf("\tInvalid choice\n");
					}
			}
	printf("\t___________________________________________________________\n");
	printf("\t                                        Total Amount\n");
	printf("\t                   			$ %d\n",bill);



	}
else
	{
	printf("\n\n\t\t\t\t      MENU");
	 printf("\n\t\t\t\t________________");
	 printf("\n ----------------------------------------------------------------------------\n");
	 printf("|\t<_STARTER_>\t\t\t|11.Coconut And\t\t\t     |");
	 printf("\n|1.Baked Ham hock\t\t\t|   Corn Curry.....................$2|\n");
	 printf("|  Pots......................$3\t\t|12.Baked Vegan\t\t\t     |\n");
	 printf("|2.Pomegranatee &\t\t\t|   Korma..........................$3|\n");
	 printf("|  Walnut Salad..............$5\t\t|13.Butternut,Chestnut\t\t     |\n");
	 printf("|3.Roasted Harissa\t\t\t|   & Lential Cake.................$6|\n");
	 printf("|  Cauliflower...............$3\t\t|\t  <_Drinks & Beverage_>      |\n");
	 printf("|4.Potted Carb...............$5\t\t|14.Tea............................$1|\n");
	 printf("|\t<_MAIN COURSE_>\t\t\t|15.Americano......................$2|\n");
	 printf("|5.Spicy Pork................$7\t\t|16.Boba...........................$2|\n");
	 printf("|6.Butter Chicken............$4\t\t|17.Milkshake......................$1|\n");
	 printf("|7.Beetroot and Onion          \t\t|18.Pepsi..........................$2|\n");
	 printf("|  Tarte.....................$4\t\t|19.Coca Cola......................$1|\n");
	 printf("|8.Chicken MO:MO.............$3\t\t|\t    <_Desserts_>\t     |\n");
	 printf("|9.Stuffed Coriander\t\t\t|20.Trifle.........................$2|\n");
	 printf("|  Pumkin....................$4\t\t|21.Ice Cream......................$1|\n");
	 printf("|10.Chicken Cheese\t\t\t|22.Macaroons......................$2|\n");
	 printf("|  Burger....................$2\t\t|23.Muffin.........................$1|\n");
	 printf(" ----------------------------------------------------------------------------\n");
	 printf("Enter the number of item\n");
	 scanf("%d",&n);
	 for(i=1;i<=n;i++)
		{
		printf("Enter the serial no. of item you want to order\n");
		scanf("%d",&item[i]);
		printf("Number of servings\n");
		scanf("%d",&x[i]);
		}
printf("Do you want to add any more item enter y for yes and n for no\n");
getchar();
scanf("%c",&b);
if(b=='y' || b=='Y')
	{
	printf("Enter the number of item you want to add\n");
	scanf("%d",&ad);
	ad=ad+n;
		for(i=n+1;i<=ad;i++)
		{
		printf("Enter the serial no. of item\n");
		scanf("%d",&item[i]);
		printf("Enter the no. of servings\n");
		scanf("%d",&x[i]);
		}
	n=ad;
	}
clrscr();
printf("\n*Press 1 to get You bill\n");
printf("*Press 2 to cancel the order\n");
scanf("%d",&c);
if(c==1)
	{
	goto aa;
	}
if(c==2)
	{
	goto bb;
	}
	aa:
	getchar();
	clrscr();
	printf("\t____________________________________________________________\n");
	printf("\t************************************************************\n");
	printf("\t                            Recepit                   \n");
	printf("\t************************************************************\n");
	printf("\t____________________________________________________________\n");
	printf("\tITEMS                     \t\tQty \tPRICE\n");

		for(i=1;i<=n;i++)
			{
					switch(item[i])
					{
					case 1:
					printf("\t%d.Baked Ham\t\t\t\t%d\t$3\n",i1,x[i]);
					printf("\t  Hock Pots\n");
					price=3*x[i];
					bill=bill+price;
					i1++;
					break;
					case 2:
					printf("\t%d.Pomegranatee &\t\t\t%d\t$5\n",i1,x[i]);
					printf("\t  Walnut Salad\n");
					price=5*x[i];
					bill=bill+price;
					i1++;
					break;
					case 3:
					printf("\t%d.Roasted Harissa\t\t\t%d\t$3\n",i1,x[i]);
					printf("\t  Cauliflower\n");
					price=3*x[i];
					bill=bill+price;
					i1++;
					break;
					case 4:
					printf("\t%d.Potted Carb\t\t\t\t%d\t$5\n",i1,x[i]);

					price=5*x[i];
					bill=bill+price;
					i1++;
					break;
					case 5:
					printf("\t%d.Spicy Pork\t\t\t\t%d\t$7\n",i1,x[i]);

					price=7*x[i];
					bill=bill+price;
					i1++;
					break;
					case 6:
					printf("\t%d.Butter Chicken\t\t\t%d\t$4\n",i1,x[i]);

					price=4*x[i];
					bill=bill+price;
					i1++;
					break;
					case 7:
					printf("\t%d.Beetroot & Onion\t\t\t%d\t$4\n",i1,x[i]);
					printf("\t  Tarte\n");
					price=4*x[i];
					bill=bill+price;
					i1++;
					break;
					case 8:
					printf("\t%d.Chicken MO:MO\t\t\t\t%d\t$3\n",i1,x[i]);

					price=3*x[i];
					bill=bill+price;
					i1++;
					break;
					case 9:
					printf("\t%d.Stuffed Coriander\t\t\t%d\t$4\n",i1,x[i]);
					printf("\t  Pumkin\n");
					price=4*x[i];
					bill=bill+price;
					i1++;
					break;
					case 10:
					printf("\t%d.Chicken Cheese\t\t\t%d\t$2\n",i1,x[i]);
					printf("\t  Burger\n");
					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 11:
					printf("\t%d.Cocunut &\t\t\t\t%d\t$2\n",i1,x[i]);
					printf("\t  Corn Curry\n");
					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 12:
					printf("\t%d.Baked Vegan\t\t\t\t%d\t$3\n",i1,x[i]);
					printf("\t  Korma\n");
					price=3*x[i];
					bill=bill+price;
					i1++;
					break;
					case 13:
					printf("\t%d.Butternut,Chestnut\t\t\t%d\t$6\n",i1,x[i]);
					printf("\t  And Lential Cake\n");
					price=6*x[i];
					bill=bill+price;
					i1++;
					break;
					case 14:
					printf("\t%d.Tea\t\t\t\t\t%d\t$1\n",i1,x[i]);

					price=1*x[i];
					bill=bill+price;
					i1++;
					break;
					case 15:
					printf("\t%d.Americano\t\t\t\t%d\t$2\n",i1,x[i]);

					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 16:
					printf("\t%d.Boba\t\t\t\t\t%d\t$2\n",i1,x[i]);

					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 17:
					printf("\t%d.Milkshake\t\t\t\t%d\t$1\n",i1,x[i]);

					price=1*x[i];
					bill=bill+price;
					i1++;
					break;
					case 18:
					printf("\t%d.Pepsi\t\t\t\t\t%d\t$2\n",i1,x[i]);

					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 19:
					printf("\t%d.Coca Cola\t\t\t\t%d\t$1\n",i1,x[i]);

					price=1*x[i];
					bill=bill+price;
					i1++;
					break;
					case 20:
					printf("\t%d.Trifle\t\t\t\t%d\t$2\n",i1,x[i]);

					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					case 21:
					printf("\t%d.Ice Cream\t\t\t\t%d\t$1\n",i1,x[i]);

					price=1*x[i];
					bill=bill+price;
					i1++;
					break;
					case 23:
					printf("\t%d.Muffin\t\t\t\t%d\t$1\n",i1,x[i]);

					price=1*x[i];
					bill=bill+price;
					i1++;
					break;
					case 22:
					printf("\t%d.Macaroons\t\t\t\t%d\t$2\n",i1,x[i]);

					price=2*x[i];
					bill=bill+price;
					i1++;
					break;
					default:
					printf("\tInvalid choice\n");
					}
			}
	printf("\t___________________________________________________________\n");
	printf("\t                                        Total Amount\n");
	printf("\t                   			$ %d\n",bill);
}
bb:
printf("\n\n\t\t\t     Press Enter to close");
getchar();
clrscr();
printf("\n\n\n\n\t\t\t\tThank You (^-^)");



getch();
}
