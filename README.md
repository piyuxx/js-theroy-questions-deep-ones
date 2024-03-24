1. Event Delegation: Event delegation is a technique used in event handling within web development to manage events more efficiently, especially in scenarios where there are multiple elements that need to have the same event handler. Instead of attaching an event handler to each individual element, event delegation involves attaching a single event handler to a common ancestor of these elements.
Example: 
<div class="container" id="buttonContainer">
    <button>Button 1</button>
    <button>Button 2</button>
    <button>Button 3</button>
</div>

<script>
    // Get the common ancestor element
    var container = document.getElementById('buttonContainer');
    // Attach a single event listener to the common ancestor
    container.addEventListener('click', function(event) {
        // Check if the clicked element is a button
        if (event.target.tagName === 'BUTTON') {
            // Log the text content of the clicked button
            console.log('Button clicked:', event.target.textContent);
        }
    });
</script>
2.  Event Bubbling (or bubbling phase):
After the event has reached the target element, it starts bubbling up through the DOM hierarchy, the bubble go from child to parent.
Example:<div class="outer" id="outer">
    Outer Div
    <div class="inner" id="inner">
        Inner Div
    </div>
</div>

<script>
    var outer = document.getElementById('outer');
    var inner = document.getElementById('inner');

    inner.addEventListener('click', function(event) {
        console.log('Inner div clicked. Event Phase: ' + event.eventPhase);
    });

    outer.addEventListener('click', function(event) {
        console.log('Document clicked. Event Phase: ' + event.eventPhase);
    });
</script>

3.capturing : During the capturing phase, the event is captured by the outermost element and propagates through the DOM hierarchy down to the target element.
Event capturing allows you to intercept an event as it moves towards its target.
Event listeners attached during the capturing phase will be triggered before the event reaches its target element.
example: outer.addEventListener('click', function(event) {
        console.log('Outer div clicked. Event Phase: ' + event.eventPhase);
    }, true); // Event capturing phase

4. This Keyword: https://codeburst.io/the-simple-rules-to-this-in-javascript-35d97f31bde3
