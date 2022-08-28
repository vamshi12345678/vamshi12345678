- 👋 Hi, I’m @vamshi12345678
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
vamshi12345678/vamshi12345678 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include<iostream>
#include<queue>
using namespace std;
class node{
    public:
 node *left;
int data;
 node *right;
 node(int te){
     left=NULL;
 this->data=te;
 right=NULL;
 }
};
 node* input(node* root){
 cout<<"enter the data"<<endl;
 int data;
 cin>>data;
 root=new node(data);
 if(data==-1){
    return NULL;
 }
 cout<<"enter the data at left side"<<data<<endl;
 root->left=input(root->left);
  cout<<"enter the data at rigth side"<<data<<endl;
  root->right=input(root->right);
  return root;

 }
 

 
 
 void preorder(node* root){
     if(root!=NULL){
         
        cout<<root->data;
         preorder(root->left);
         preorder(root->right);
         
         
         
         
     }
     
     
     
     
     
 }
 void inorder(node* root){
     
     
     if(root!=NULL){
      inorder(root->left);
         cout<<root->data;
         inorder(root->right);
         
         
         
         
     }
     
     
     
 }
 void postorder(node* root){

     if(root!=NULL){
        
         postorder(root->left);
         postorder(root->right);
           cout<<root->data;
         
         
         
     }
     
     
     
     
 }
 
 void print(node* root){
     int i=0;
     queue<node*> q;
     q.push(root);
     q.push(NULL);
     while(!q.empty()){
        node* temp=q.front();
        q.pop();
        if(temp==NULL){
            cout<<endl;
        if(!q.empty()){
            q.push(NULL);
        }


     }
     else{
        cout<<temp->data<<" "<<i++;
        if(temp->left){
            q.push(temp->left);
        }
                if(temp->right){
            q.push(temp->right);
        }



     }
     }
