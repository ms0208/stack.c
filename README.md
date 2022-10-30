# stack.c
// Linear Stack.
#include<stdio.h>
#include<conio.h>
void push(int A[],int *Top, int size){
    if(*Top==size-1){

        printf("Overflow\n");
    }
    else{
       (*Top)++;
       printf("Enter the element\n");
       scanf("%d",&A[*Top]);
    }
}
void pop(int A[],int *Top){
    if(*Top==-1){
        printf("Underflow\n");
    }
    else{
        printf("Delete elements %d \n",A[*Top]);
       (*Top)--;
    }
}
void transverse(int A[],int Top){
    int i;
    if(Top==-1){
        printf("Underflow\n");
    }
    else{
        for(i=Top;i>=0;i--){
            printf("%d\t",A[i]);
        }
    }
    
} 
void main() 
{
    int A[20],size,choice,Top;
    int ch;
     Top = -1;
    printf("Enter your size of stack\n");
    scanf("%d",&size);
    do{
        printf("Main Menu\n");
        printf("Enter 1 for push\n");
        printf("Enter 2 for pop\n");
        printf("Enter 3 for transverse\n");
        printf("Enter 0 for exit\n");
        printf("Enter your choice\n");
        scanf("%d",&choice);
      switch(choice){
            case 1:
             push(A,&Top,size);
            break;
            case 2:
            pop(A,&Top);
            break;
            case 3:
            transverse(A,Top);
            break;
            case 4:
            printf("good bye");
            break;
            default:
            printf("Invalid");
    }
        printf("Do you want continue press 7");
        scanf("%d",&ch);
    }while(ch==7);
    getch();
}
