/* linked list are implimented as queue 
     new nodes are added from back or rear end
     and deletion takes place at the front end
*/

#include <iostream>

using namespace std;

// class node...................................................................................

class node{
           private:
             int data;
           public:
             node *next;
             node(int);
             int getdata();
};           

int node::getdata(){
 return data;
}

node::node(int d){
 data = d;
 next = NULL;
}
 
//class linkedList...............................................................................
class linkedList{
                 private:
                   node *start, *end; 
                 public:
                   linkedList();
                   void addNode(int);
                   void insertNode(int, int);
                   void deleteNode();
                   void display();
};


linkedList::linkedList(){
 start = NULL;
 end = NULL;
}

void linkedList::addNode(int d)
{
 node *tmp = new node(d);
 if(start==NULL)
           start = end = tmp;
         
 else      {
             end->next = tmp; 
             end = tmp;
           }   
}


void linkedList::insertNode(int dt, int pos)
{
 node *newNode = new node(dt);
 node *tmp = start;
 node *prev;
 if(pos == 1) 
     {
        newNode->next = start;
        start = newNode;
     }
 else 
 {
    for(int i=1; i<pos; ++i)
    {
       if(i == pos-2) prev = tmp; 
       tmp = tmp->next;
    }
    prev->next = newNode;
    newNode->next = tmp;
 }
}

void linkedList::deleteNode()
{
 cout << "\n\n\n\n\n\nBefore deletion :";
 this->display();
 if(start==NULL&&end==NULL)
       cout << "\nNO ElEMENT IN LIST.!!"; 
 else{
       node *tmp = start;
       start = start->next;
       delete tmp;
     }
 cout << "\n\n\n\nAfter deletion :";
 this->display();
}


void linkedList::display()
{
 node *tmp = start;

 cout << "\nDisplaying all nodes of this linked list.\n";
 if((start==NULL) && (end==NULL))
        cout << "\nNothing to display.\n";
 else if(start==end) cout <<"\nOnly one node present. Node deta :"<< tmp->getdata();
 else 
     while(tmp->next != NULL)
        {
           cout << "\nNode data :"<< tmp->getdata();
           tmp = tmp->next;
        }
     cout << "\nNode data :"<< tmp->getdata();
}


int main()
{
 char ch;
 int datum, choice, index;
 linkedList One;
 cout << "\nHello!!."<<"\ntest program.\nSuccessfully created a linked list.\n";
do{
 cout << "\nYou can do following functions:\n1.Add Node\n2.Insert Node\n3.Delete Node\n4.Display (Displays all elements in linked list)\n";
 cout << "\nEnter your choice :";
 cin >> choice;
 switch(choice)
 {
  case 1 : cout << "\nAdding node, give the parameter for the node ( an integer): ";
           cin >> datum;
           One.addNode(datum);
           break;
  case 2 : cout << "\nInserting node, give the parameter for the node ( an integer): ";
           cin >> datum;
           cout << "\nGive the position or index ( given that starting node is marked one/1) of insertion :";
           cin >> index;
           One.insertNode(datum, index);
           break;
  case 3 : cout << "\nDeleting from front end.";
           One.deleteNode();
           break;
  case 4 : One.display();
           break;
  default :cout << "\nWrong choice...";
 }
 cout << "\nDo you want to repeat? ( y or n)";
 cin >> ch;

}while(ch=='y'||ch=='Y');
 
 return 0;
}
