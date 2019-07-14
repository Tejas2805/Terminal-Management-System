#include<stdio.h>
#include<string.h>
int a1[3],a2[3],a3[3],a4[3],a5[3],a6[3],m[3];
int x1, x2, x3, x4, x5, x6, k;
char ch, temp[50];;
char name1[3][50],name2[3][50],name3[3][50],name4[3][50],name5[3][50], name6[3][50];
int lane; int f;

void input()
{
	int i;
	for(i=0;i<3;i++)
	{
		a1[i]=0;
		a2[i]=0;
		a3[i]=0;
		a4[i]=0;
		a5[i]=0;
		a6[i]=0;
	}
	x1=0;
	x2=0;
	x3=0;
	x4=0;
	x5=0;
	x6=0;
}

void landing()
{
	int p;
	printf("\nEnter priority between 1 and 3, 1 being closest to runway and 3 farthest\n");
	scanf("%d",&p);
	switch(p)
	{
		case 1:
			   enterA();
			   break;
		case 2:
			   enterB();
			   break;
		case 3:
			   enterC();
			   break;
		default:
			   printf("\nIncorrect value of priority entered\n");
			   break;
	}
}

void enterA()
{
	
	if(x1<=1)
	{
		printf("\nEnter the name of the plane : ");
		scanf("%s",&name1[x1]);
		a1[x1]=1;
		x1++;
		printf("\nPlane entered in lane 1");
	}
	else if(x2<=1)
	{
		printf("\nEnter the name of the plane : ");
		scanf("%s",&name2[x2]);
		a2[x2]=1;
		x2++;
		printf("\nPlane entered in lane 2");
	}	
	else if(x1>1&&x2>1&&x3<=1)
	{
		printf("Shifting previous plane from lane 1 to lane 3 to make place for current priority requirement");
		for(k=0;k<50;k++)
		{
			name3[x3][k]=name1[x1-1][k];
		}
		printf("\nEnter the name of the new plane : ");
		scanf("%s",&name1[x1-1]);
		a3[x3]=1;
		x3++;
		printf("\nPlane entered in lane 1");
	}
	else if(x1>1&&x2>1&&x3>1&&x4<=1)
	{
		printf("Shifting previous plane from lane 1 to lane 4 to make place for current priority requirement");
		for(k=0;k<50;k++)
		{
			name4[x4][k]=name1[x1-1][k];
		}
		printf("\nEnter the name of the new plane : ");
		scanf("%s",&name1[x1-1]);
		a4[x4]=1;
		x4++;
		printf("\nPlane entered in lane 1");
	}
	else if(x1>1&&x2>1&&x3>1&&x4>1&&x5<=1)
	{
		printf("Shifting previous plane from lane 2 to lane 5 to make place for current priority requirement");
		for(k=0;k<50;k++)
		{
			name5[x5][k]=name2[x2-1][k];
		}
		printf("\nEnter the name of the new plane : ");
		scanf("%s",&name2[x2-1]);
		a5[x5]=1;
		x5++;
		printf("\nPlane entered in lane 2");
	}
	else if(x1>1&&x2>1&&x3>1&&x4>1&&x5>1&&x6<=1)
	{
		printf("Shifting previous plane from lane 2 to lane 6 to make place for current priority requirement");
		for(k=0;k<50;k++)
		{
			name6[x6][k]=name2[x2-1][k];
		}
		printf("\nEnter the name of the new plane : ");
		scanf("%s",&name2[x2-1]);
		a6[x6]=1;
		x6++;
		printf("\nPlane entered in lane 2");
	}
	else if(x1>1&&x2>1&&x3>1&&x4>1&&x5>1&&x6>1&&a1[x1]==0)
	{
		printf("All lanes occupied. Request to fill special empty slot? Enter Y to confirm, any key to decline\n");
		scanf(" %c",&ch);
		if(ch=='y'||ch=='Y')
		{
			printf("Request accepted. Plane moved to special slot of lane 1.\n");
			printf("Enter the name of new plane in special slot : ");
			scanf("%s",&name1[x1]);
			a1[x1]=1;
		}
		else
		{
			printf("Request denied. No further space available for this priority at this terminal\n");
		}
	}
	else if(x1>1&&x2>1&&x3>1&&x4>1&&x5>1&&x6>1&&a1[x1]==1&&a2[x2]==0)
	{
		printf("All lanes occupied. Request to fill special empty slot? Enter Y to confirm, any key to decline\n");
		scanf(" %c",&ch);
		if(ch=='y'||ch=='Y')
		{
			printf("Request accepted. Plane moved to special slot of lane 2.\n");
			printf("Enter the name of new plane in special slot : ");
			scanf("%s",&name2[x2]);
			a2[x2]=1;
		}
		else
		{
			printf("Request denied. No further space available for this priority at this terminal\n");
		}
	}
	else
	{
		printf("All requested slots in current priority lane are occupied, including special slot. Shifting cannot occur. Please divert aircraft to less prior lane.");
	}
	printf("\n");
}

void enterB()
{
	
	if(x3<=1)
	{
		printf("\nEnter the name of the plane : ");
		scanf("%s",&name3[x3]);
		a3[x3]=1;
		x3++;
		printf("\nPlane entered in lane 3");
	}
	else if(x4<=1)
	{
		printf("\nEnter the name of the plane : ");
		scanf("%s",&name4[x4]);
		a4[x4]=1;
		x4++;
		printf("\nPlane entered in lane 4");
	}
	else if(x3>1&&x4>1&&x5<=1)
	{
		printf("Shifting previous plane from lane 3 to lane 5 to make place for current priority requirement");
		for(k=0;k<50;k++)
		{
			name5[x5][k]=name3[x3-1][k];
		}
		printf("\nEnter the name of the new plane : ");
		scanf("%s",&name3[x3-1]);
		a5[x5]=1;
		x5++;
		printf("\nPlane entered in lane 3");
	}
	else if(x3>1&&x4>1&&x5>1&&x6<=1)
	{
		printf("Shifting previous plane from lane 4 to lane 6 to make place for current priority requirement");
		for(k=0;k<50;k++)
		{
			name6[x6][k]=name4[x4-1][k];
		}
		printf("\nEnter the name of the new plane : ");
		scanf("%s",&name4[x4-1]);
		a6[x6]=1;
		x6++;
		printf("\nPlane entered in lane 4");
	}
	else if(x3>1&&x4>1&&x5>1&&x6>1&&a3[x3]==0)
	{
		printf("All lanes occupied. Request to fill special empty slot? Enter Y to confirm, any key to decline\n");
		scanf(" %c",&ch);
		if(ch=='y'||ch=='Y')
		{
			printf("Request accepted. Plane moved to special slot of lane 3.\n");
			printf("Enter the name of new plane in special slot : ");
			scanf("%s",&name3[x3]);
			a3[x3]=1;
		}
		else
		{
			printf("Request denied. No further space available for this priority at this terminal\n");
		}
	}
	else if(x3>1&&x4>1&&x5>1&&x6>1&&a3[x3]==1&&a4[x4]==0)
	{
		printf("All lanes occupied. Request to fill special empty slot? Enter Y to confirm, any key to decline\n");
		scanf(" %c",&ch);
		if(ch=='y'||ch=='Y')
		{
			printf("Request accepted. Plane moved to special slot of lane 4.\n");
			printf("Enter the name of new plane in special slot : ");
			scanf("%s",&name4[x4]);
			a4[x4]=1;
		}
		else
		{
			printf("Request denied. No further space available for this priority at this terminal\n");
		}
	}
	else
	{
		printf("All requested slots in current priority lane are occupied, including special slot. Shifting cannot occur. Please divert aircraft to less prior lane.");
	}
	printf("\n");
}

void enterC()
{
	
	if(x5<=1)
	{
		printf("\nEnter the name of the plane : ");
		scanf("%s",&name5[x5]);
		a5[x5]=1;
		x5++;
		printf("\nPlane entered in lane 5");
	}
	else if(x6<=1)
	{
		printf("\nEnter the name of the plane : ");
		scanf("%s",&name6[x6]);
		a6[x6]=1;
		x6++;
		printf("\nPlane entered in lane 6");
	}
	else if(x5>1&&x6>1&&a5[x5]==0)
	{
		printf("All lanes occupied. Request to fill special empty slot? Enter Y to confirm, any key to decline\n");
		scanf(" %c",&ch);
		if(ch=='y'||ch=='Y')
		{
			printf("Request accepted. Plane moved to special slot of lane 5.\n");
			printf("Enter the name of new plane in special slot : ");
			scanf("%s",&name5[x5]);
			a5[x5]=1;
		}
		else
		{
			printf("Request denied. No further space available for this priority at this terminal\n");
		}
	}
	else if(x5>1&&x6>1&&a5[x5]==1&&a6[x6]==0)
	{
		printf("All lanes occupied. Request to fill special empty slot? Enter Y to confirm, any key to decline\n");
		scanf(" %c",&ch);
		if(ch=='y'||ch=='Y')
		{
			printf("Request accepted. Plane moved to special slot of lane 6.\n");
			printf("Enter the name of new plane in special slot : ");
			scanf("%s",&name6[x6]);
			a6[x6]=1;
		}
		else
		{
			printf("Request denied. No further space available for this priority at this terminal\n");
		}
	}
	else
	{
	printf("All requested slots in current priority lane are occupied, including special slot. Shifting cannot occur. Please divert aircraft to less prior lane.");
	}	
	printf("\n");
}

void takeoff()
{
	printf("The flights are :\n\n");
	f=1; int i;
	for(i=0;i<3;i++)
	{
		if(a1[i]==1)
       	{
       		
			 printf("%d. %s\n",f,&name1[i][0]);
		
		f++;
	}
}
	for(i=0;i<3;i++)
	{
	if(a2[i]==1)
       	{	
       		
			 printf("%d. %s\n",f,&name2[i][0]);
		
		f++;
	}
}
	for(i=0;i<3;i++)
	{
		if(a3[i]==1)
       		{
			   
			 printf("%d. %s\n",f,&name3[i][0]);
		
		f++;
	}
}
	for( i=0;i<3;i++)
	{
		if(a4[i]==1)
       	{
       		
			 printf("%d. %s\n",f,&name4[i][0]);
		
		f++;
	}
}
	for(i=0;i<3;i++)
	{
		if(a5[i]==1)
       	{
       		
			 printf("%d. %s\n",f,&name5[i][0]);
		
		f++;
	}
}
	for(i=0;i<3;i++)
	{
	if(a6[i]==1)
       	{
			 printf("%d. %s\n",f,&name6[i][0]);
		
		f++;
	}
}
if(f==1)
{
	printf("All slots are empty.");
}
else 
{
	int choice;
	printf("Enter choice\n");
	scanf("%d",&choice);
	if(choice>=1 && choice<=f)
	{
	int q=slot(choice);
	rearrange(q);
	printf("\n");
}
	else
	{
		printf("Wrong Choice!\n");
	}
}
}

int slot(int b)
{
	int c=0; int i;
	for( i=0;i<3;i++)
	{
		if(a1[i]==1)
		c++;
		if(c==b)
		{
			lane=i;
			return 1;
		}
		
	}
	for( i=0;i<3;i++)
	{
		if(a2[i]==1)
		c++;
		if(c==b)
		{
			lane=i;
			return 2;
		}
		
	}
	for( i=0;i<3;i++)
	{
		if(a3[i]==1)
		c++;
		if(c==b)
		{
			lane=i;
			return 3;
		}
		
	}
	for(i=0;i<3;i++)
	{
		if(a4[i]==1)
		c++;
		if(c==b)
		{
			lane=i;
			return 4;
		}
		
	}
	for( i=0;i<3;i++)
	{
		if(a5[i]==1)
		c++;
		if(c==b)
		{
			lane=i;
			return 5;
		}
		
	}for( i=0;i<3;i++)
	{
		if(a6[i]==1)
		c++;
		if(c==b)
		{
			lane=i;
			return 6;
		}
		
	}
}

void rearrange(int h)
{
	int i; int a=0;
	if(lane==0)
		a=-1;
	switch(h)
	{
	
		case 1:
							printf("The flight %s in lane 1 slot %d has taken off\n",&name1[lane][0],lane);
			if(lane==0)
			{
				for(i=lane+1;i<3;i++)
				{
					a++;
					m[a]=a1[i];
					strcpy(&name1[a][0],&name1[i][0]);
					
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a1[i]=m[b];
				b++;
			}
			a1[b]=0;
			for(i=0;i<50;i++)
			{
				name1[b][i]='\0';
			}
		}
		else if(lane==1)
		{
			for(i=lane+1;i<3;i++)
				{
					strcpy(&name1[lane][0],&name1[i][0]);
					m[a]=a1[i];
					a++;
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a1[i]=m[b];
				b++;
			}
			a1[b+1]=0;
			for(i=0;i<50;i++)
			{
				name1[b][i]='\0';
			}
		}
		else
		{
			a1[2]=0;
			for( i=0;i<50;i++)
			{
				name1[2][i]='\0';
			}
		}
		break;
	case 2:
						printf("The flight %s in lane 2 slot %d has taken off\n",&name2[lane][0],lane);
			if(lane==0)
			{
				for(i=lane+1;i<3;i++)
				{
					a++;
					m[a]=a2[i];
					strcpy(&name2[a][0],&name2[i][0]);
					
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a2[i]=m[b];
				b++;
			}
			a2[b]=0;
			for(i=0;i<50;i++)
			{
				name2[b][i]='\0';
			}
		}
		else if(lane==1)
		{
			for(i=lane+1;i<3;i++)
				{
					strcpy(&name2[lane][0],&name2[i][0]);
					m[a]=a2[i];
					a++;
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a2[i]=m[b];
				b++;
			}
			a2[b+1]=0;
			for(i=0;i<50;i++)
			{
				name2[b][i]='\0';
			}
		}
		else
		{
			a2[2]=0;
			for( i=0;i<50;i++)
			{
				name2[2][i]='\0';
			}
		}
		break;
				  
	case 3:
							printf("The flight %s in lane 3 slot %d has taken off\n",&name3[lane][0],lane);
			if(lane==0)
			{
				for(i=lane+1;i<3;i++)
				{
					a++;
					m[a]=a3[i];
					strcpy(&name3[a][0],&name3[i][0]);
					
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a3[i]=m[b];
				b++;
			}
			a3[b]=0;
			for(i=0;i<50;i++)
			{
				name3[b][i]='\0';
			}
		}
		else if(lane==1)
		{
			for(i=lane+1;i<3;i++)
				{
					strcpy(&name3[lane][0],&name3[i][0]);
					m[a]=a3[i];
					a++;
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a3[i]=m[b];
				b++;
			}
			a3[b+1]=0;
			for(i=0;i<50;i++)
			{
				name3[b][i]='\0';
			}
		}
		else
		{
			a3[2]=0;
			for( i=0;i<50;i++)
			{
				name3[2][i]='\0';
			}
		}
		break;
	case 4:
		printf("The flight %s in lane 4 slot %d has taken off\n",&name4[lane][0],lane);
			if(lane==0)
			{
				for(i=lane+1;i<3;i++)
				{
					a++;
					m[a]=a4[i];
					strcpy(&name4[a][0],&name4[i][0]);
					
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a4[i]=m[b];
				b++;
			}
			a4[b]=0;
			for(i=0;i<50;i++)
			{
				name4[b][i]='\0';
			}
		}
		else if(lane==1)
		{
			for(i=lane+1;i<3;i++)
				{
					strcpy(&name4[lane][0],&name4[i][0]);
					m[a]=a4[i];
					a++;
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a4[i]=m[b];
				b++;
			}
			a4[b+1]=0;
			for(i=0;i<50;i++)
			{
				name4[b][i]='\0';
			}
		}
		else
		{
			a4[2]=0;
			for( i=0;i<50;i++)
			{
				name4[2][i]='\0';
			}
		}
		break;
				  
	case 5:
	printf("The flight %s in lane 5 slot %d has taken off\n",&name5[lane][0],lane);
			if(lane==0)
			{
				for(i=lane+1;i<3;i++)
				{
					a++;
					m[a]=a5[i];
					strcpy(&name5[a][0],&name5[i][0]);
					
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a5[i]=m[b];
				b++;
			}
			a5[b]=0;
			for(i=0;i<50;i++)
			{
				name5[b][i]='\0';
			}
		}
		else if(lane==1)
		{
			for(i=lane+1;i<3;i++)
				{
					strcpy(&name5[lane][0],&name5[i][0]);
					m[a]=a5[i];
					a++;
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a5[i]=m[b];
				b++;
			}
			a5[b+1]=0;
			for(i=0;i<50;i++)
			{
				name5[b][i]='\0';
			}
		}
		else
		{
			a5[2]=0;
			for( i=0;i<50;i++)
			{
				name5[2][i]='\0';
			}
		}
		break;
	case 6:
	printf("The flight %s in lane 6 slot %d has taken off\n",&name6[lane][0],lane);
			if(lane==0)
			{
				for(i=lane+1;i<3;i++)
				{
					a++;
					m[a]=a6[i];
					strcpy(&name6[a][0],&name6[i][0]);
					
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a6[i]=m[b];
				b++;
			}
			a6[b]=0;
			for(i=0;i<50;i++)
			{
				name6[b][i]='\0';
			}
		}
		else if(lane==1)
		{
			for(i=lane+1;i<3;i++)
				{
					strcpy(&name6[lane][0],&name6[i][0]);
					m[a]=a6[i];
					a++;
				}
			int b=0;
			for(i=lane;i<=a;i++)
			{
				a6[i]=m[b];
				b++;
			}
			a6[b+1]=0;
			for(i=0;i<50;i++)
			{
				name6[b][i]='\0';
			}
		}
		else
		{
			a6[2]=0;
			for( i=0;i<50;i++)
			{
				name6[2][i]='\0';
			}
		}
		break;
				  
}
}

void display()
{
	int i;
	printf("\nLANE 1\n");
	for(i=0;i<3;i++)
	{
		if(a1[i]==1)
			printf(" Slot %d : Occupied by plane %s \n",i,name1[i]);
		else
			printf(" Slot %d : Empty \n");
	}
	printf("LANE 2\n");
	for(i=0;i<3;i++)
	{
		if(a2[i]==1)
			printf(" Slot %d : Occupied by plane %s \n",i,name2[i]);
		else
			printf(" Slot %d : Empty \n");
	}
	printf("LANE 3\n");
	for(i=0;i<3;i++)
	{
		if(a3[i]==1)
			printf(" Slot %d : Occupied by plane %s \n",i,name3[i]);
		else
			printf(" Slot %d : Empty \n");
	}
	printf("LANE 4\n");
	for(i=0;i<3;i++)
	{
		if(a4[i]==1)
			printf(" Slot %d : Occupied by plane %s \n",i,name4[i]);
		else
			printf(" Slot %d : Empty \n");
	}
	printf("LANE 5\n");
	for(i=0;i<3;i++)
	{
		if(a5[i]==1)
			printf(" Slot %d : Occupied by plane %s \n",i,name5[i]);
		else
			printf(" Slot %d : Empty \n");
	}
	printf("LANE 6\n");
	for(i=0;i<3;i++)
	{
		if(a6[i]==1)
			printf(" Slot %d : Occupied by plane %s \n",i,name6[i]);
		else
			printf(" Slot %d : Empty \n");
	}
	printf("\n");
} 


int main()
{
	printf("*********************************************************************************\n");
	printf("		WELCOME TO THE AIRPORT TERMINAL MANAGEMENT SYSTEM					\n");
	printf("*********************************************************************************");
	printf("\n");
	input();
	ch='Y'; int c;
	do
	{
		printf("\nEnter your Choice\n1. Landing\n2. Take-off\n3. Display\n\n");
		scanf("%d",&c);
		switch(c)
		{
			case 1:
				landing();
				break;
			case 2:
                takeoff();
              	break;
			case 3:
				display();
				break;
			default: 
				printf("\nIncorrect choice entered! Please choose between 1 to 3.\n");
				break;
	}
		
		printf("\nWould you like to continue? Enter y to continue, any key to exit\n");
		scanf(" %c",&ch);
	}while(ch=='Y'||ch=='y');
	
	
	return 0;
}

