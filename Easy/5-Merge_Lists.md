/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode() : val(0), next(nullptr) {}
 *     ListNode(int x) : val(x), next(nullptr) {}
 *     ListNode(int x, ListNode *next) : val(x), next(next) {}
 * };
 */

```
class Solution {
public:
    ListNode* mergeTwoLists(ListNode* list1, ListNode* list2) {
           
        //if list-1 is empty then print elemnets of list-2
        if(list1 == NULL)
            return list2;
        //if list-2 is empty then print elemnets of list-1
        if(list2 == NULL)
            return list1;
        
        //Merge the list in sorted order
        if(list1->val <= list2->val){
            list1->next = mergeTwoLists(list1->next,list2);     //recursive call
            
            return list1;
        }
        else{
            list2->next = mergeTwoLists(list1,list2->next);    //recursive call
            
            return list2;
        }
        
    }
};
```
