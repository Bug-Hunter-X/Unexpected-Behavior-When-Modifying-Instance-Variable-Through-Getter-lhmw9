# Ruby Instance Variable Modification Through Getter

This repository demonstrates an uncommon bug in Ruby related to modifying instance variables through getter methods.  The bug arises from a misunderstanding of how Ruby handles instance variable assignment within getter methods.  Attempting to modify the returned value of a getter method does not modify the instance variable itself.

## Bug Description
The provided Ruby code defines a `MyClass` with an instance variable `@value`. A getter method `value` is created to access `@value`.  The code demonstrates that although it seems possible to reassign a value via the getter, it does not change the instance variable's value. This often goes unnoticed, leading to unexpected program behavior.

## Solution
The solution involves either directly modifying the instance variable or creating a dedicated setter method.