# Merge-Sort-on-a-Linked-List

1: ll -> middle
2: 1) left half 
   2) right half
   mid.next = null
3: merge

1) mid //finding method ---> for even we are considering mid the first half last node

  slow = head
  fast = head.next [// if here we have intilize fast with only head then we get the mid at the starting of second half bascially the slow pointer is there, when fast has covered full length]
  while(fast != null && fast.next != null){
        slow -> +1
        fast -> +2
  }
  slow -> middle Node
 
 2) rightHead = mid.next
    mid.next = null
    mS(head) //left half
    mS(rH) //right half

3)  head1, head2
    Node mergedLL = new Node(-1)
    Node temp = mergedLL
    while(h1 != null && h2 != null) {
        h1 <--> h2
    }
    head1 == head2 == null
    return mergedLL.next