														Project 6
													Multiset Design

1.Introduction

In my gamming scenario I will be using a Virtual Reality game headset (like the one you use in Meta Quest) 
where I play as a medieval warrior with multiple types of inventory items which will include, but not limited to, 
a sword,  an ax,  a mace,  a bow and arrow, coins, keys (many of which will have different shapes and colors),  
maps, potions( each specifically will do different things depending on the potion itself), etc. each item will 
be sorted in separate types of sequences. For example, the weapons such as the sword, ax, and bow and arrow will 
all be in a sequence called "Weapons", while the potions, or any magical items with the ability to be used to 
regenerate lost stamina or increase stats such as Hit points, speed, or attack strength, will be in a sequence 
called "StatChangers". I could have sequence variable called "PotionIngredients" that holds ingredients so my 
avatar could use them to brew potions. My multiset's sole purpose is to store strings or titles of each item 
in the game.

2. Design Philosophy
   
In my reality game, the users would be people who would play headsets like Meta quest, and they would be the 
ones using my multiset (or bag). In my multiset (which I’m just going to declare it as "bag" for this scenario) I 
would have an integer that represents the number of objects in my bag called "SizeOfMultiList" that would be 
incremented or decremented when you either add or subtract objects from it. To make my multiset more readable and 
simpler to use, when I want to access the data in my bag I just use my set of sequences that will be used to help 
organize my objects in them based on how many times I've used them. If I want to remove it all I have to do is select 
it from the menu and press the drop button and I can tell it how many of that object I wish to eliminate permanently.

3.Core Operations

A good operation any multiset would support would be "bagRemove(x)" to remove an object in my bag based on my "x" parameter 
or "bagAdd(x)" to add something to it, which is also based on my "x" parameter. Both of these operations use 0(n). Another 
operation any multiset would use is "bagShuffle()" to randomly reorganize each and every item in my bag. This would require 
a time complexity of 0(n). The final operation I can think of that a multiset would use is to grab the first object that 
is on the list such as "bagGrab()", which would have a time complexity of 0(1).

4.Set Operations

The first operation I would use in my virtual reality game is to label a key item such as a weapon or an 
actual key from any item in my bag that is useful for the game quest. So that way if I press a button on my 
controller, such as select, I can immediately use that object without having to go to my bag and look for the 
object, which can be a little time consuming. The time complexity should be 0(n). This would be done by having 
my program check each individual item until it hits the object that is labeled as "REGISTERED".  The second 
operation I would use is for each of my potion ingredients in the bag. I would make a method that calculates 
which potion ingredients that is most likely to be used for a given moment in the game. For example, for a dragon 
boss battle, the computer may be more concerned about you getting burned. Or if you want to battle an enemy with 
high stats, you would need a potion that would require your stats to be greatly increased. It would most likely use 
recursion for this scenario which would most likely make the time complexity for this method to be 0(log n). 

5. Extension Feature
   
The code for the first method I would make is "void activateRegistered()" which is no dought used to activate the 
labeled item in my multiset. The code for the second method I made would be "Potion BrewPotion(List of Ingredients)" 
that would return a potion object so all the ingredients in the parameter ( which will be sorted in a vector) will 
be turned into a potion.

6. UML Diagram / Abstraction Boundary
   
The UML of my multiset called "Bag"
			![alt text](BagUML.png)

   
   

The advantages of both Sequences and AVLTrees
			![alt text](dataChart.png)

   
   

Complexities of Sequences and AVLTrees
			![alt text](dataChartB.png)


7. Trade-off Analysis
   
The data structure I have chosen to use is a sequence and I will be comparing it to a AVL tree. I chose 
to use a sequence(1) mainly because it is simpler and has more flexibility for its data, as well as its 
ease of use and accessing its data can be quite efficient especially if it is a priority queue rather 
than just a vector or a array list. Though it does have some disadvantages such as more prone to wasted 
memory(3) and can also lead to memory leaks. Using a AVL tree does have advantages such efficient 
searching(2) making retrieving data more quickly and efficient in most scenarios, also there is quicker 
insertion and deletion. However, the disadvantage of using a tree is that it requires a lot of memory to 
use and if the tree is not balanced it can result in uneven search times. Another disadvantage is its 
complexity which can be difficult to understand for the person writing the code of my game. That is why 
I would prefer using a sequence for my game making it more simpler for my code writer because I normally 
value simplicity. If I wanted to go back and degub my code, then fixing any errors should be much simpler 
then using Hashtables or AVLTrees.


8. Alternative Design Sketch
    
If I had used the other types of data structures, such as, HashTable or AVLTrees, organizing each item 
that comes out of my bag might be a bit different than using a sequence. If I chose to use a HashTable 
each item might be organized in a more unexpected way, Hashtables organize their elements based on a 
number system such as integers, but the game programmer might not be able to understand how each object 
will be organized and will be  randomly sorted which might cause frustration to the player. Using sequences 
is a bit more predictable and less stressful since all you have to do is look at each element in the bag 
one by one until you find the correct item. Using AVLTrees would probably be better than using HashTables 
but not better than sequences. Using AVLTrees might organize the items with less predictability especially 
if you have to constantly balance each item in the tree not knowing exactly how they are organized. Also, 
it should be noted that coding a AVL tree if more complicated than a sequence(I would know because the part 
of coding an AVLTree that was most stressful for me was balancing the tree after every insertion or removal). 
	


9. Evaluation Plan
    
If I were to test the data structures of my virtual world game I would hire a beta tester that would 
test each part of my game and when you are doing certain sections of the game, such as brewing a potion 
or fighting a medieval dragon, you would need to have access to your items in the bag that are organized 
using my sequence. If my tester feels that using a sequence is not the best approach to organizing the 
elements of my bag then I would not hesitate changing up and using any one of my other data structures. 
However, if both my game tester is truly satisfied with the results then I truly feel that the extensibility 
and maintainability of my bag is well organized and implemented.

10. Conclusion / Reflection
    
My bag would be a strong and effective multiset due to the abstraction(4) of it. In the UML chart 
of my bag, you would see that the only method that is public is my LootItem method because I want the 
bad guys in my game to snatch an item from my character and in order to do this, they need access to 
a method in my player's bag class which needs to be a public interphase for it to be possible. However, 
the other method and the variables are all private because I only want my player to have access to them 
and no other class, including other players in my game, should be allowed to manipulate the data 
in their game.


Documentation
Written by: 
	Tyler
	Raymond
	Harvey


1. https://www.bing.com/search?q=c%2B%2B+advantages+of+using+sequences&form=ANNTH1&refig=6925f596ec854fd496fa2dd4de84c1ef&pc=LCTS
2. https://www.geeksforgeeks.org/dsa/applications-advantages-and-disadvantages-of-tree/
3. https://www.bing.com/search?q=c%2B%2B%20disadvantages%20of%20using%20sequences&qs=n&form=QBRE&sp=-1&lq=0&pq=c%2B%2B%20disadvantages%20of%20using%20sequences&sc=8-36&sk=&cvid=8818C15EE6B049148E26EA0D1D8426A0
4. https://en.wikipedia.org/wiki/Abstraction_(computer_science)
	
