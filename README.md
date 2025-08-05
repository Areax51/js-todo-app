# Todo App – Technical & Functional Specification

## 1. Overview / Purpose  
A lightweight Todo App that enables users to **add, edit, delete, toggle, and filter** tasks, with data **persisted via localStorage**. The app will work in modern browsers and support mobile-first responsive design.

## 2. User Stories & Acceptance Criteria  
Using the standard template: *As a user, I want … so that …*

- **As a user**, I want to add a new task so that I can track things I need to do.  
  - Acceptance: When I type a task name and click "Add", it appears in the list and saves to localStorage.
  
- **As a user**, I want to edit an existing task so that I can correct mistakes or adjust tasks.  
  - Acceptance: Clicking an edit icon replaces the task with an input field, and changes are saved and persisted.

- **As a user**, I want to mark tasks as completed so that I can distinguish between done and undone tasks.  
  - Acceptance: Clicking a checkbox toggles task strike-through and status, and this persists across reloads.

- **As a user**, I want to delete a task so unwanted items can be removed from my list.  
  - Acceptance: Clicking delete removes the task and updates localStorage.

- **As a user**, I want to filter tasks by All / Active / Completed so I can easily manage my workflow.  
  - Acceptance: Filter buttons update the view and maintain filter selection on page refresh.

## 3. Non-Functional Requirements  
- The app must be **responsive**, adapting to mobile screens (<600px) using CSS Flexbox or Grid.  
- UI should remain **fast**, even with hundreds of tasks (i.e. minimal DOM updates).  
- Must work **offline** using localStorage, without network dependencies.  
- Clean, semantic markup with accessibility in mind (meaningful buttons, ARIA labels where needed).

## 4. Data Flow & Storage  
- Tasks are stored in localStorage as an array of objects:  
  ```json
  [
    { id: "uuid", text: "Do laundry", completed: false }
  ]
