# My Document with Mermaid

This is some regular text before the Mermaid diagram.

```mermaid
graph TD
    A[Start] --> B{Decision};
    B -- Yes --> C[Process 1];
    B -- No --> D[Process 2];
    C --> E[End];
    D --> E;

print("Hello, world!")
print("Goodbye, world!)
