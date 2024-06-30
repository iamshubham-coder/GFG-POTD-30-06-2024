# GFG-POTD-30-06-2024
DELETE IN DOUBLY LINKEDLIST AT SPECIFIC LOCATION


class Solution {
  public:
    Node* deleteNode(Node* head, int x) {
        if(x==1) return head->next;
        int cnt = 1;
        Node * temp = head;
        while(temp->next != NULL && cnt < x){
            temp=temp->next;
            cnt++;
        }
        temp->prev->next=temp->next;
        delete temp;
        return head;
    }
};
