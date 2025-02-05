# 📌 Test-Driven Development (TDD) Approach for TMS

## Objective

Adopt TDD to build a reliable and maintainable Task Management System (TMS). By writing tests **before** implementation, you ensure that every feature is defined by its expected behavior.

## TDD Cycle: Red – Green – Refactor

1. **Write a Failing Test (Red)**

   - Start with a clear, small piece of functionality.
   - Write a unit test that describes the expected behavior.
   - Run the test suite and see it fail (confirming the test works).

2. **Write Minimal Code to Pass the Test (Green)**

   - Implement the simplest solution that makes the test pass.
   - Keep the implementation simple; do not add extra functionality.
   - Run the tests to ensure the new code passes.

3. **Refactor**

   - Clean up the code while keeping tests green.
   - Remove duplication, improve naming, and optimize performance.
   - Re-run the tests frequently during refactoring.

4. **Repeat**
   - Move to the next piece of functionality by writing another failing test.
   - Continue the cycle until the feature is complete.

## Applying TDD to Our Project

### Example: Task Creation Component

#### 1. Write a Test

- **Test Scenario:** When a user submits a new task via `TaskForm`, it should add a new task to the task list.
- **Sample Test (using Jest & React Testing Library):**

  ```javascript
  // src/tests/TaskForm.test.js
  import { render, screen, fireEvent } from "@testing-library/react";
  import TaskForm from "../components/TaskForm";

  test("adds a new task when form is submitted", () => {
    const mockAddTask = jest.fn();
    render(<TaskForm addTask={mockAddTask} />);

    // Simulate user input
    const input = screen.getByPlaceholderText(/task title/i);
    fireEvent.change(input, { target: { value: "New Task" } });

    // Simulate form submission
    const button = screen.getByRole("button", { name: /add task/i });
    fireEvent.click(button);

    // Expect mockAddTask to have been called with the new task
    expect(mockAddTask).toHaveBeenCalledWith(
      expect.objectContaining({
        title: "New Task",
      })
    );
  });
  ```

- Run the test and observe that it fails (since the component is not yet implemented).

#### 2. Implement Minimal Code

- Implement the `TaskForm` component so that the above test passes.

  ```javascript
  // src/components/TaskForm.jsx
  import { useState } from "react";

  function TaskForm({ addTask }) {
    const [title, setTitle] = useState("");

    const handleSubmit = (e) => {
      e.preventDefault();
      if (!title.trim()) return;
      addTask({ id: Date.now(), title, status: "To Do" });
      setTitle("");
    };

    return (
      <form onSubmit={handleSubmit}>
        <input
          type="text"
          placeholder="Task Title"
          value={title}
          onChange={(e) => setTitle(e.target.value)}
        />
        <button type="submit">Add Task</button>
      </form>
    );
  }

  export default TaskForm;
  ```

  - Run the tests and ensure they pass.

#### 3. Refactor

- Once tests are passing, review the code for clarity and maintainability.
- Refactor any repetitive logic or improve naming conventions.
- Continue to run tests after each change to ensure nothing breaks.

## Broader TDD Guidelines for TMS

### Unit Testing Components:

- Write tests for each component (e.g., Login, Dashboard, TaskDetails) before implementation.
- Test component behavior, state changes, and user interactions.

### Integration Testing:

- Write tests that simulate full user flows (e.g., creating and viewing a task).
- Use React Testing Library to verify that components work together as expected.

### End-to-End (E2E) Testing:

- Use Cypress (or a similar tool) to simulate real user behavior.
- Test the app’s navigation, form submissions, and overall user experience.

### Mocking & Test Data:

- For Phase 1, mock API calls and use localStorage or in-memory data for persistence.
- Use libraries like msw (Mock Service Worker) to simulate network requests if needed.

### Continuous Integration (CI):

- Integrate your tests into your CI pipeline (e.g., via GitHub Actions) to run tests automatically on each commit.
- This ensures ongoing confidence in your TDD approach.

### Benefits of TDD

- **Early Bug Detection:** Catch issues before they make it into production.
- **Improved Design:** Forces you to think about the API and behavior of your components.
- **Refactoring Safety:** Tests provide a safety net during code refactoring.
- **Documentation:** Tests serve as living documentation for expected behavior.

### Tools to Use

- **Jest:** For running JavaScript tests.
- **React Testing Library:** For testing React components in a user-centric way.
- **Cypress:** For E2E testing (optional for initial phases).
- **Mock Service Worker (msw):** For mocking API calls.

### Next Steps

- **Implement TDD for Each Feature:** Follow the TDD cycle for each component and integration point.
- **Review & Refactor Regularly:** Use the tests as a guide to refactor code without fear of breaking functionality.
- **Integrate into CI:** Ensure tests are part of your build process for continuous feedback.

By following this TDD approach, you’ll build a robust, well-tested Task Management System that can easily scale and adapt as new features are integrated, especially when moving from frontend-only to backend integration.

## Final Note

Integrate these TDD guidelines into your overall development plan (refer to **05_Development_Plan.md** and **06_Testing_Strategy.md**). This way, each feature is built with tests in mind, ensuring higher code quality and easier maintenance throughout your project lifecycle.
