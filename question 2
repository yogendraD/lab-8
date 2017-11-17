#include<iostream>

using namespace std;

// .....................................................................................
class node{
           private:
             int data;
           public:
             node *link;
             node(int);
             int getdata();
};

int node::getdata(){
 return data;
}

node::node(int d){
 data = d;
 link = NULL;
}

//.....................................................................................

class Stack{
             private:
                   node *bottom, *top;
             public:
                   Stack();
                   void Push(int);
                   void Pop();
                   void display();
};


Stack::Stack(){
 bottom = NULL;
 top = NULL;
}

void Stack::Push(int d)
{
 node *tmp = new node(d);
 if(top==NULL)
           bottom = top = tmp;

 else      {
             tmp->link = top;
             top = tmp;
           }
}


void Stack::Pop()
{
 cout << "\n\n\n\n\n\nBefore deletion :";
 this->display();
 if(bottom==NULL && top==NULL)
       cout << "\nNO ElEMENT IN STACK.!!";
 else{
       node *tmp = top;
       top = top->link;
       delete tmp;
     }
 cout << "\n\n\n\nAfter deletion :";
 this->display();
}


void Stack::display()
{
 node *tmp = top;

 cout << "\nDisplaying all nodes of this stack.\n";
 if((bottom==NULL) && (top==NULL))
        cout << "\nNothing to display.\n";
 else if(bottom==top) cout <<"\nOnly one node present. Node deta :"<< tmp->getdata();
 else
     while(tmp->link != NULL)
        {
           cout << "\nNode data :"<< tmp->getdata();
           tmp = tmp->link;
        }
     cout << "\nNode data :"<< tmp->getdata();
}




int main()
{
 char ch;
 int datum, choice, index;
 Stack One;
 cout << "\nHello!!."<<"\nSuccessfully created a Stack.\n";
do{
 cout << "\nYou can do following functions:\n1.Add Node (Push)\n2.Delete Node ( Pop)\n3.Display (Displays all elements in the stack)\n";
 cout << "\nEnter your choice :";
 cin >> choice;
   switch(choice)
   {
     case 1 : cout << "\nAdding node, give the parameter for the node ( an integer): ";
              cin >> datum;
              One.Push(datum);
              break;
     case 2 : cout << "\nDeleting from rear end.";
              One.Pop();
              break;
     case 3 : One.display();
              break;
     default :cout << "\nWrong choice...";
   }
   cout << "\nDo you want to repeat? ( y or n)";
   cin >> ch;

  }while(ch=='y'||ch=='Y');

 return 0; 
}

