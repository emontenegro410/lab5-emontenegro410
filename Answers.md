Answer the following questions:
Why does LinkedStack not require an explicit constructor?
LinkedStack doesn't require an explicit constructor because the appropriate constructor methods are in the Node class and they are called when needed during the push() function. The interface also gives us the appropriate methods.

What is the time and (extra) space complexity of each of the LinkedStack methods, as well as ReverseLines.main?
`ReverseLines.main`?
`E push(final E obj)`- O(1) time, O(1) space
`E peek()`- O(1) time, O(1) space
`E pop()`- O(1) time, O(1) space
`boolean isEmpty()`- O(1) time, O(1) space
`List<E> asList()`- O(n) time, O(n) space
`ReverseLines`- O(n) time, O(n) space


How else (not using Node) could we have implemented LinkedStack in such a way that it is still based on a linked list but the asList method uses constant time and space?

   - How else (not using `Node`) could we have implemented `LinkedStack` in such a way that it is still based on a linked list but the `asList` method uses constant time and space?
    -We could implement it using an ArrayList<> using the indices as nodes- we would restrict operations to the front of the array to simulate a linked list structure. This way, we could return the ArrayList itself during the asList function. Also, the space would be limited to what already exists in the linked list structure.


Is it better for push and pop to return the item or the stack itself? Briefly discuss the pros and cons of each design.

   - Is it better for `push` and `pop` to return the item or the stack itself?
    Briefly discuss the pros and cons of each design.
    It is better to return the item when pushing and popping. This is because when we push or pop, we are usually doing it on a per element basis, rather than to see the change in the whole structure at once. Receiving the whole structure in return would defeat the purpose of the LIFO implementation, since we should only be concerned with stuff that is happening at the top. Also, when we pop we do it for purposes like iterating through the stack and printing all the elements- this would be more cumbersome if we received a whole list in return, because then we would be iterating through that list anyways. If you wanted to do large operations involving the whole stack itself perhaps returning the stack itself would be better.
