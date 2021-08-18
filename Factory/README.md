# Factory
### also known as _Virtual Constructor_

*Factory* is an desing pattern that provide an interface for creating objects.

## Use Case
You have an program that manage and logistical system, and until now you just dealed with transport by truck, and you use an specific and big class named Truck for it. Now you need to deal with outher type of transport, as example Ships. Includ ship on this logical can be an chalenge, and maybe change all the base of your code.

### Solution for this case
This desing pattern can solve this problem. In this pattern you won't construct you object directly, but you'll use an spcesial method made just for this, that will return an object referred as _products_ for you use, like a magic.

Now you can deal with all the method calls intern using subclass, for instance: the method *deliver* called outside of the class, can call intent others method especific for each transport, like *TruckDeliver* or *ShipDeliver*.
The code outside the class is the same for any transport, and any addition of a new transport would just need a new subclass.

## When use this pattern
* When you don't know all the type of dependencies of the objects that you'll work. 
* When you need save resource reusing the same object insted of remake them all the time, specially for bigs objects.

## Pros and Cons

:heavy_check_mark: Single Responsibility Principle. You can make easier to suport, moving the code of creation in a specific place.

:heavy_check_mark: Open/Closed Principle. You can add new types of products without breaking existing code.

:x: The code can be complicated, because you can add alot of subclasses to implement this pattern.