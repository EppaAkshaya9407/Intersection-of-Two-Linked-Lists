# Intersection-of-Two-Linked-Lists
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None
class Solution:
    def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> Optional[ListNode]:
        if headA is None or headB is None:
            return None
        c=None
        temp=headA
        a1=[]
        while temp:
            a1.append(temp)
            temp=temp.next
        a2=[]
        temp1=headB
        while temp1:
            a2.append(temp1)
            temp1=temp1.next
        n=min(len(a1),len(a2))
        for i in range(1,n+1):
            if a1[-i]==a2[-i]:
                c=a1[-i]
            else:
                break
        return c
