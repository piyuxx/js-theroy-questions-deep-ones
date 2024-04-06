1. Event Delegation: Event delegation is a technique used in event handling within web development to manage events more efficiently, especially in scenarios where there are multiple elements that need to have the same event handler. Instead of attaching an event handler to each individual element, event delegation involves attaching a single event handler to a common ancestor of these elements.

2.  Event Bubbling (or bubbling phase):
After the event has reached the target element, it starts bubbling up through the DOM hierarchy, the bubble go from child to parent.

3.capturing : During the capturing phase, the event is captured by the outermost element and propagates through the DOM hierarchy down to the target element.
Event capturing allows you to intercept an event as it moves towards its target.
Event listeners attached during the capturing phase will be triggered before the event reaches its target element.
example: outer.addEventListener('click', function(event) {
        console.log('Outer div clicked. Event Phase: ' + event.eventPhase);
    }, true); // Event capturing phase

4. This Keyword: https://codeburst.io/the-simple-rules-to-this-in-javascript-35d97f31bde3

5. Explain how prototypal inheritance works
All JavaScript objects have a __proto__ property with the exception of objects created with Object.create(null), that is a reference to another object, which is called the object's "prototype". When a property is accessed on an object and if the property is not found on that object, the JavaScript engine looks at the object's __proto__, and the __proto__'s __proto__ and so on, until it finds the property defined on one of the __proto__s or until it reaches the end of the prototype chain.

6.What do you think of AMD vs CommonJS?
Both are ways to implement a module system, which was not natively present in JavaScript until ES2015 came along. CommonJS is synchronous while AMD (Asynchronous Module Definition) is obviously asynchronous. CommonJS is designed with server-side development in mind while AMD, with its support for asynchronous loading of modules, is more intended for browsers.
