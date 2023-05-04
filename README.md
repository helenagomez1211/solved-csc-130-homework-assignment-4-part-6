Download Link: https://assignmentchef.com/product/solved-csc-130-homework-assignment-4-part-6
<br>
The motivation behind this problem is to practice implementing binary trees and understand how stacks  are used by compilers to implement recursion. You will be writing a sorting algorithm. You will first insert all the integer keys to be sorted into an initially empty binary search tree T, and then traverse T toretrieve the keys in sorted order. But instead of implementing the traversal recursively, you will use astack.a. You can use your stack implementation from the previous assignment but you may need to update the type stored. You are also allowed to use Java’s Stack.b. Implement a binary search tree class. Each node in your implementation should have fields for a key and left and right subtrees but should not have a parent reference. The methods in the BSTincludei. Return the key at the rootii. Return the left subtree of the rootiii. Return the right subtree of the rootiv. Test if the tree is emptyv. Construct an empty treevi. Test if the tree contains a given valuevii. Insert a new Integer into the BST1. In the Weiss book there is an example insertion method. Your method will be similar but you must support duplicate values.

Your method will be similar but you must support duplicate values.

/*

Internal method to insert into a subtree.

@param x the item to insert.

@program t the node that roots the subtree.

@return the new root of the subtree.

*/

Private BinaryNode&lt;AnyType&gt; insert(AntType x, BinaryNode&lt;&gt;AnyType)

{

If ( t== null)

Return new BinaryNode&lt;&gt; ( x, null, null);

int compareResult = x.compareTo ( t.element );

if ( CompareResult &lt; 0 )

t.left = insert ( x, t.left );

else if ( compareREsult &gt; 0 )

t.right = inser ( x, t.right );

else

;     // Duplicate, do nothing

return t;

}

c. What type of tree traversal do you need to implement to retrieve the keys from your binary search tree in sorted order? Implement it without recursion, instead

using your stack to simulate the recursion.

i. Hints: What type of object needs to be stored on the stack? Exactly which object needs to be pushed when you are about to start the traversal of the left subtree? When do you pop the stack and what do you do with the result that is popped? What do you do when the stack is empty?

d. Implement a class called SortIntegers. Include a method called “sortIntegerArray” which will take as an argument an array of Integers, it will then insert them into the binary search tree class you implemented above, then use the tree traversal method you implemented in part c to sort the integers.

Return an array of the Integers sorted.

e. You are not required to turn in any testing methods.