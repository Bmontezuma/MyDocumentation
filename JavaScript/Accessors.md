![Image](https://i.morioh.com/2021/10/26/677043de.webp)
# ***Accessors***

***Accessors*** in JavaScript, often referred to as "***getters***" and "***setters***," are functions used to access and modify object properties. They provide a way to control how properties are accessed and set. Here are some comprehensive notes on ***accessors*** in JavaScript:

## ***Getter Function***:

- A ***getter function*** allows you to retrieve the value of a property.
 - It is defined using the ***`get`*** keyword followed by the ***property name***.
- ***Getter functions*** are invoked without using parentheses as if they were properties.
```javascript
const obj = {
    get propertyName() {
        return this._propertyName;
    },
    _propertyName: 42
};

console.log(obj.propertyName); // Output: 42
```

## ***Setter Function***:

- A ***setter function*** allows you to set the value of a property.
- It is defined using the ***`set`*** keyword followed by the ***property name***.
- ***Setter functions*** take one parameter, which represents the value being assigned to the property.
```javascript
const obj = {
    _propertyName: 0,
    set propertyName(value) {
        if (value > 0) {
            this._propertyName = value;
        }
    }
};

obj.propertyName = 42;
console.log(obj.propertyName); // Output: 42

obj.propertyName = -1; // Setter function prevents setting negative values
console.log(obj.propertyName); // Output: 42
```

## ***Usage***:

- ***Accessors*** are useful for ***implementing computed properties***, ***data validation***, or ***side effects*** when getting or setting a property.
- They provide a way to hide the implementation details of a property, thus encapsulating it.
- ***Getters*** can be used to compute a value based on other properties.
- ***Setters*** can be used to enforce constraints or trigger actions when a property is modified.

## ***Computed Properties***:

***Getters*** allow the creation of ***computed properties***, where the value is determined dynamically.
```javascript
const obj = {
    _firstName: 'John',
    _lastName: 'Doe',
    get fullName() {
        return `${this._firstName} ${this._lastName}`;
    }
};

console.log(obj.fullName); // Output: John Doe
```

## ***Private Properties***:

***Accessors*** can be used to implement private properties by convention, although JavaScript does not have built-in support for private members.
```javascript
const obj = (() => {
    let _privateProperty = 42;

    return {
        get privateProperty() {
            return _privateProperty;
        },
        set privateProperty(value) {
            _privateProperty = value;
        }
    };
})();

console.log(obj.privateProperty); // Output: 42
obj.privateProperty = 100;
console.log(obj.privateProperty); // Output: 100
```

## ***Considerations***:

- ***Accessors*** should not have side effects beyond property access or assignment.
- Avoid expensive computations or I/O operations within ***getters*** as they can impact performance.
- Use ***accessors*** judiciously, preferring simple properties when no additional logic is required.
- By understanding and leveraging ***accessors***, you can write more expressive and encapsulated code in JavaScript, enhancing readability and maintainability.





