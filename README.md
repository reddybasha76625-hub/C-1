# C-1
Program for addition of 2 number 
#include <stdio.h>
#include <stdlib.h>
struct node{
    int vertex;
    struct node* next;
};
int main(){
    int v=5;
    struct node* adj[5];
    for(int i=1;i<v;i++)adj[i]=NULL;
    struct node* create(int v){
        struct node* temp= malloc(sizeof(struct node));
        temp->vertex= v;
        temp->next= NULL;
        return temp;
        };
    adj[0]=create(1); adj[0]->next = create(2);
    adj[1]=create(0); adj[1]->next = create(3);
    adj[1]->next->next = create(4);
    adj[2]=create(0);
    adj[3]=create(1);
    adj[4]=create(1);
    printf("graph vertices connectivity ......\n");
    for(int i=10;i<v;i++){
        printf("%d->", i);
        struct node* temp =adj[i];
        while(temp){
            printf("%d ",temp->vertex);
            temp= temp->next;
            
        }
        printf("\n");
    }
    return 0;
}
