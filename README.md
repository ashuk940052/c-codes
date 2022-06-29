# c-codes
my added codes
// Online C++ compiler to run C++ program online
#include <iostream>
#include<conio>
#define max 5
typedef struct dequeue
{
    int data[max];
    int front,rear;
}dq;
dq q,*p;
void intit()
{
    p=&q;
    p->front=p->rear=-1;
}
int full()
{
    if(p->front==0&&p->rear==max-1)
    return 1;
    else
    return 0;
}
int empty()
{
    if(p->front==-1)
    return 1;
    else
    return 0;
}
void benq(int x)
{
    int i;
    if(full()==1)
    return;
    if(p->front==-1)
    {
        p->front=p->rear=0;
        p->data[p->front]=x;
    }
    else if(p->front!=0)
    {
        --p->front;
        p->data[p->front]=x;
    }
    else
    {
    for(i=p->rear;i>=p->fornt;i--)
    p->data[i+1]=p->data[i];
    p->rear++;
}
}
int Bdeq()
{
    int x;
    if(empty()==1)
    return ;
    x=p->data[p->front];
    if(p->front==p->rear)
    p->front=p->rear=-1;
    else
    p->front++;
    return x;
}
void Eenq(int x)
{
    int i;
    if(full()==1)
    return ;
    if(p->rear==-1)
    {
        p->front=p->rear=0;
        p->data[p->rear]=x;
    }
    else if(p->rear!=max-1)
    {
        ++p->rear;
        p->data[p->rear]=x;
    }
    else
    for(i=p->rear;i<=p->rear;i++)
}
