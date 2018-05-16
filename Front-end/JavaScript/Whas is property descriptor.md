## What is property descriptor?
The simplest way to add a property to an existing object is through the following notation:

    `objectName`.`propertyName` = value;
There is the second approach which can give us a little bit more flexibility. It's called property descriptor. Example:

    var car = {
      name: "Audi R8",
    }
    
    Object.defineProperty(car, "currentSpeed", {value: 60, writable: false, enumerable: true});
    
    
    console.log(car);

Note! If you provide an object for property configuration you should remember that all configuration properties which you don't specify are false by default. 

Configuration properties:
1. Value - what is the value of the property?
2. writable: true/false - can someone change the value of the property?
3. enumerable: true/false - can our users see this property or it's hidden?
4. configurable: true/false - can we redefine the property with another defineProperty overriding(it will throw an error if we try)?
