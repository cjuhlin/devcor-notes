\#SOLID

# SOLID

## S.O.L.I.D

### Single responsibilty

Make things (classes, functions, etc.) responsible for fulfilling one type of role. 

````
e.g. Refactor code responsibilities into separate classes.
````

For example, if you have a shop and make a purchase. Then the first thing you need is to make an order and then payment. So in this case the order handling like what item and how many and what price can be part of the order class but the payment should be separated from the order class.  This is because if you example you want to add other payment methods to the shop you only need to change the payment class to support additional payment methods. 

### Open-closed principle

Be able to add new functionality to existing code easily without modifying existing code.

````
e.g. Use abstract classes. These can define what subclasses will require and strengthen Principle 1. by separating code duties.
````

For example, you have a payment processor to handle payment as a class, so if you want to add a new payment method you create a subclass of the payment processor for that payment option instead of modifying the payment processor class with the payment method. 

### Liskov substitution principle

When a class inherits from another class, the program shouldn't break and you shouldn't need to hack anything to use the subclass.

````
e.g. Define constructor arguments to keep inheritance flexible.
````

For example, if you have credit card payment and want to add PayPal payment as an option.  The difference between the credit card and PayPal payment is that credit card needs a security code and PayPal needs an email to complete the payment. So the payment processors should not have a dependency of security code in itself but instead, it should be required by the credit card subclass of the payment processor and email should be a requirement of the PayPal subclass as well. 

### Interface segregration principle

Make interfaces (parent abstract classes) more specific, rather than generic.

````
e.g. Create more interfaces (classes) if needed and/or provide objects to constructors.
````

For example, if some payment method is dependent on SMS authorization but some aren't. So you can't add it directly to the payment processor (this will also break the [Liskov substitution principle](SOLID.md#liskov-substitution-principle) as well). But instead, you make a new interface that is a subclass of the payment processor that has the SMS authorization ability so the payment method that needs the SMS authorization uses the new subclass instead of the payment processor class. In this way, it will not break the payment method that doesn't have SMS authorization. Another way is to separate the SMS authorization to its class instead of having it inside the payment processor which is a better design choice and use the new SMS auth class in the payment method that needs it. 

### Dependency inversion principle

Make classes depend on abstract classes rather than non-abstract classes.

````
e.g. Make classes inherit from abstract classes.
````

For example, if you have created an SMS authorizer class and using it in your payment method class directly and wanted to add another way to authorize then is better to make an authorizer class and make the SMS authorizer to a subclass of the authorizer class instead and use it inside the payment method class in this way is easier to switch between which authorize method you want to use. 
