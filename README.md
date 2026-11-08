# Week 5 Assignment: DOM Manipulation - Interactive To-Do List

## Live Project Link
* **Live Demo:** [Click Here to View My Live GitHub Pages Site](https://github.io)

## Specific Lessons Learned

1. **The Core Advantage of Event Delegation:** I learned that assigning one global single click event listener directly onto a parent wrapper node container (such as `#todo-list`) is significantly more efficient than binding a loop of custom individual tracking listeners onto each newly spawned child component. This structural pattern ensures that dynamically generated task objects register micro-interactions immediately upon creation without needing manual re-binding cycles.
2. **Defensive Programming Against Cross-Site Scripting (XSS):** I learned that parsing continuous inputs using `.textContent` securely mitigates client-side injection entry points. While raw assignments through `.innerHTML` can accidentally compile string arrays as live executables (such as unexpected `<img src="x" onerror="...">` warning frames), `.textContent` forces strings to print strictly as inert literal values.
3. **Data-State Synchronicity:** I discovered that mutations should be applied directly to a clean database array layer (`let todos = []`) before triggering a centralized, procedural `.render()` update view. Mutating UI text content values directly from HTML strings risks corrupting active data states.
