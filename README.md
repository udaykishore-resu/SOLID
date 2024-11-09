__Why do we need SOLID?__

SOLID is a set of OOP principles to avoid dependencies between code components. If the code has a lot of dependencies such code is hard to maintain.

The main problems solid principles resolves are:

_Fragility_: Change in one part breaks the work of other parts.

_Immobility_: code cannot be reused outside of its context.

_Rigidity_: Each change causes many other changes.


__Single Responsibility__ 

Each class should have one goal, and all its methods should work to achieve that goal. If any of its method is not fit to achieve that goal, It will be moved else where.

Lets take below User class a example, the User class job is to give information about the user like name, email, subscription details.

[Single responsibility](Java/blob/main/SOLID/SingleResponsibility/User.java)

If you look at the above example, the hasExtraAccess method checks if the User has extra access to the content based on the subscription type.
But its look like User class has two roles; one is _providing user information_ and the second one is _content access based on subscription_.
This is against the Single Responsibility Principle.

Lets remove hasExtraAccess method from User class, write it in a different class.




