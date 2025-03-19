*Review Guidelines for Task -2*


### **Self-Introduction & Project Explanation**

- Begin by asking the student to introduce themselves briefly.
- Ask them to **explain what they have built** in their project.
    - Encourage them to walk through their code, describing its functionality.
    - Ask what challenges they faced and how they solved them.

**1. DOM - The Document Object Model**

- How you use JavaScript to modify a website
- the DOM is a programming interface that lets JavaScript dynamically change the content, structure, and style of a webpage
-  A **structured representation** of an HTML document. When a webpage loads, the browser converts the HTML code into a **tree-like structure**, where each element (like `<div>`, `<p>`, `<button>`, etc.) becomes a **node** in this tree.

JavaScript can interact with this **DOM tree** to **read, modify, add, or remove elements** dynamically, without needing to reload the page.

## **Example**  
If your HTML page has this button:

```html
<button id="myButton">Click Me</button>
```
You can use JavaScript to change its text:

```jsx
document.getElementById("myButton").innerText = "Clicked!";
```
**2. Event Listeners (If Used)**

- If they have used event listeners, ask:
    - **How does an event listener work?**
        
        An event listener is a method that listens for user interactions (such as clicks, key presses, or form submissions) and executes a function when the specified event occurs.
        
        It is typically added using the `addEventListener` method.
        
        **If the student struggles, explain:**
        
        - `"addEventListener"` is used to attach an event to an element.
        
        ```jsx
        document.getElementById("btn").addEventListener("click", function() {
        console.log("Button Clicked!");
        });
        ```
        
    - **Which event(s) have you handled in your project?**
    The student should mention the events they used in their project
    - **Can you explain how your event listener is triggering a function?**
    The event listener is attached to an element and waits for the event to occur.
    When the event happens, the function inside the listener executes.
        
        If they struggle, guide them by explaining how `addEventListener` works with an example.
        In the explanation check whether they understood the concept of anonymous function
        
    - **Ask to move if any inline css has been used in js code**
    eg: Adding .delete-btn style to the element created inside js.
    `deleteButton.classList.add("delete-btn");`
    - **Have you used browser console for debugging ?**
    if they are not aware, show them the browser console
    - If they haven’t added either of delete, add or mark as complete ask them to add it on live
    (make them do a small task in live. may be ask them to add a delete all or clear all button)
    - check if they understand the fundamental selector types

       1)  **element selector** (also known as a **type selector**) — this is a selector that directly matches an HTML element name. To target all paragraphs in the document, you would use the selector `p`.
    
       2) To select a subset of the elements without changing the others, you can add a `class` to your HTML element and target that class in your CSS. In your CSS, you can target the class of `special` by creating a selector that starts with a period.
    
         `.special {
        color: orange;
        font-weight: bold;
        }`
    
    3) ability to style things based on their state. This has different states depending on whether it is unvisited, visited, being hovered over, focused via the keyboard, or in the process of being clicked (activated).
    
        `button:hover{
        background: #bfc69c;
        }`
    4) symbol (#) is used to select elements by their ID attribute.
    - Use `defer` for external scripts when possible
    <script defer src="script.js"></script>
    
    drawback of placing Scritpt tag at the end - Delays script downloading until HTML parsing reaches that point.
    pros of using defer attribute - 
        can place script in <head> or elsewhere
        downloads script in parallel

### **3. Introduction to Local Storage**

- Explain that **localStorage is a way to store data persistently in the browser**.
- **Show it in action** via the browser console:
    1. **Demonstrate localStorage clearing:** 
         `localStorage.clear();`
        - Show them that all stored data is removed.
    2. **Store a key-value pair:**
    `localStorage.setItem("mydata", "example for learning");`
        - Navigate to the **Application tab** in DevTools → **Local Storage** section.
        - Show that the data is now saved.
    3. **Refresh the page** and show that the data still persists.
    4. **Explain:**
        - Unlike session storage, local storage keeps data **even after closing the browser**.
        - It works like a **mini database** but is limited in size.


### **4. Wrap-Up & Next Steps**

- Give feedback on their work:
    - What they did well.
    - Areas they can improve.
- Assign a **mini challenge**: 
    - Implement local storage to save and retrieve their To-Do list. (if they haven't implemented local storage)
