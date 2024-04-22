```mermaid
graph TD;
    A[Browser] -->|Fetch HTML, CSS, JS| B((Server))
    B -->|Responds with HTML, CSS, JS| A
    A -->|Execute JavaScript| C{Browser}
    C -->|Fetch JSON data| B
    B -->|Responds with JSON data| C
    C -->|Manipulate DOM| A
    A -->|Submit form data| B
    B -->|Handle form submission| A
