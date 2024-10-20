#include <stdio.h>  
  
int max_node = 15;  
char tree[] = {'\0', 'D', 'A', 'F', 'E', 'B', 'R', 'T', 'G', 'Q', '\0', '\0', 'V', '\0', 'J', 'L'};  
  
int get_right_child(int index){  
  if (tree[index] != '\0' && ((2 * index) + 1) <= max_node)  
    return (2 * index) + 1;  
  return -1;  
}  
  
int get_left_child(int index){  
  if (tree[index] != '\0' && (2 * index) <= max_node)  
    return 2 * index;  
  return -1;  
}  
  
void preorder(int index){  
  if (index > 0 && tree[index] != '\0'){  
    printf(" %c ", tree[index]);  
    preorder(get_left_child(index));  
    preorder(get_right_child(index));  
  }  
}  
  
void postorder(int index){  
  if (index > 0 && tree[index] != '\0'){  
    postorder(get_left_child(index));  
    postorder(get_right_child(index));  
    printf(" %c ", tree[index]);  
  }  
}  
  
void inorder(int index){  
  if (index > 0 && tree[index] != '\0'){  
    inorder(get_left_child(index));  
    printf(" %c ", tree[index]);  
    inorder(get_right_child(index));  
  }  
}  
  
int main() {  
  printf("Preorder:\n");  
  preorder(1);  
  printf("\nPostorder:\n");  
  postorder(1);  
  printf("\nInorder:\n");  
  inorder(1);  
  printf("\n");  
  return 0;  
} 

OUTPUT:
 

USING LINKED LIST

#include <stdio.h>  
#include <stdlib.h>  
  
struct node  
{  
    char data;  
    struct node *right_child;  
    struct node *left_child;  
};  
  
struct node* new_node(char data)  
{  
    struct node *temp;  
    temp = malloc(sizeof(struct node));  
    temp -> data = data;  
    temp -> left_child = NULL;  
    temp -> right_child = NULL;  
  
    return(temp);   
}  
  
void preorder(struct node *root)  
{  
    if(root != NULL)   
    {  
        printf(" %c ", root -> data);   
        preorder(root -> left_child);  
        preorder(root -> right_child);  
    }  
}  
  
void postorder(struct node *root)  
{  
    if(root != NULL)  
    {  
        postorder(root -> left_child);   
        postorder(root -> right_child);   
        printf(" %c ", root -> data);   
    }  
}  
  
void inorder(struct node *root)  
{  
    if(root != NULL)   
    {  
        inorder(root -> left_child);   
        printf(" %c ", root -> data);   
        inorder(root -> right_child);  
    }  
}  
  
int main()  
{  
    struct node *root;   
    root = new_node('D');   
  
    root -> left_child = new_node('A');  
    root -> right_child = new_node('F');   
    root -> left_child -> left_child = new_node('E');   
    root -> left_child -> right_child = new_node('B');  
  
    printf("Preorder:\n");  
    preorder(root);  
    printf("\n");  
    printf("Postorder:\n");  
    postorder(root);  
    printf("\n");  
    printf("Inorder:\n");  
    inorder(root);  
    printf("\n");  
  
    return 0;  
} 

