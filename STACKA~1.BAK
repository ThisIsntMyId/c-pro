#include<stdio.h>
#include<malloc.h>
#define max 100

struct list
{
	int info;
	struct list *next;
};
typedef struct list node;

void push(int x,node **q);
void show(node **q);
int checkin(int x,node **q);
void pop(node **q);
void peep(node **q);

int main ()
{
	node *p;
	p=NULL;
	clrscr();

	push(11,&p);
	push(22,&p);
	push(33,&p);
	push(44,&p);
	push(55,&p);
	push(66,&p);
	show(&p);
	pop(&p);
	show(&p);
	peep(&p);

	getch();

}



void push(int x,node **q)
{
	node *temp,*r;

	r=(node*)malloc(sizeof(node*));
	r->info = x;
	r->next = NULL;

	temp = *q;

	if(temp==NULL)
		*q = r;
	else
	{
		r->next = *q;
		*q=r;
	}
}

void show(node **q)
{
	node *temp;

	temp = *q;
	printf("\n ");
	if(temp==NULL)
		printf("\n ll is empty");
	else
	{

		while(temp!=NULL)
		{
			printf("%d ",temp->info);
			temp=temp->next;
		}

	}
}

int checkin(int x,node **q)
{
	node *temp;

	temp=*q;

	if(temp==NULL)
		printf("\nlinkd list is empty :(\n");
	else
	{
		while(temp!=NULL)
		{
			if(temp->info==x)
				return 1;

			temp=temp->next;
		}
	}

	return 0;
}

void pop(node **q)
{
	node *temp,*r;

	temp = *q;

	if(temp==NULL)
		printf("\n list is already empty");
	else
	{
		*q = temp->next;
		free(temp);
	}
}

void peep(node **q)
{
	
	node temp = *q;
	printf("\n%d",temp->info);
}