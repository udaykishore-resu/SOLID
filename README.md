__Why do we need SOLID?__

SOLID is a set of OOP principles to avoid dependencies between code components. If the code has a lot of dependencies such code is hard to maintain.

The main problems solid principles resolves are:

_Fragility_: Change in one part breaks the work of other parts.

_Immobility_: code cannot be reused outside of its context.

_Rigidity_: Each change causes many other changes.


__Single Responsibility__ 

Each class should have one goal, and all its methods should work to achieve that goal. If any of its method is not fit to achieve that goal, It will be moved else where.

Lets take below User class a example, the User class job is to give information about the user like name, email, subscription details.

[Non Single responsibility](https://github.com/udaykishore-resu/Java/blob/main/SOLID/SRP/User.java)

If you look at the above example, the hasExtraAccess method checks if the User has extra access to the content based on the subscription type.
But its look like User class has two roles; one is _providing user information_ and the second one is _content access based on subscription_.
This is against the Single Responsibility Principle.

Lets remove hasExtraAccess method from User class, write it in a different class as below.

[Single Responsibility](https://github.com/udaykishore-resu/Java/blob/main/SOLID/SRP/OttSubscription.java)

__Open closed principle__
OCP states that the software entities are open for extensions but should be closed for modification.
Which means you should be able to add the new functionality with out altering the existing functionality because adding a new functionality by modifying existing code leads to bugs and hard to maintain.

For an example consider the calculateInterest method of BankAccount class.

[Non OpenClosedPrinciple](https://github.com/udaykishore-resu/Java/blob/main/SOLID/OCP/BankAccount.java)

There is a problem with the calculateInterest method. What if there is a new account type introduced with new interest requirement, We have to add another if condition in the calculateInterest method. It violates OCP. 
The easiest way to fix this problem is creating a common interface for all account types and implement it for every account types.







