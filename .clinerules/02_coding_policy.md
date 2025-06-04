# Coding Policy for Recipe Sharing App

## 1. General Principles

- **Test-Driven Development (TDD):**  
  - Write tests before writing production code.
  - Each feature, bugfix, or refactor should start with a failing test.
  - Only write enough code to make the test pass.

- **Code Quality:**  
  - Use TypeScript for type safety.
  - Follow consistent code style (Prettier, ESLint).
  - Use meaningful variable and function names.
  - Keep functions and components small and focused.

- **Version Control:**  
  - Use feature branches for new work.
  - Write clear, descriptive commit messages.
  - Pull requests must pass all tests and code review before merging.

---

## 2. Testing Strategy

### **Unit Tests**
- **Tools:**  
  - Use [Jest](https://jestjs.io/) for unit testing.
  - Use [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/) for React components.
- **Coverage:**  
  - All business logic, utility functions, and React components must have unit tests.
  - Aim for >90% code coverage.
- **Location:**  
  - Place unit tests alongside the code (`*.test.ts` or `*.test.tsx`).

### **End-to-End (E2E) Tests**
- **Tools:**  
  - Use [Cypress](https://www.cypress.io/) or [Playwright](https://playwright.dev/) for E2E testing.
- **Coverage:**  
  - Critical user flows (registration, login, recipe CRUD, sharing) must have E2E tests.
- **Location:**  
  - Place E2E tests in `/e2e/` at the project root.
- **Playwright Test Loop Policy:**  
  - Always check that `npx playwright test` passes without error before considering work complete.
  - If there are errors, review code changes, fix issues, and rerun the tests.
  - This fix-and-rerun loop must be executed at least 3 times if there are test failures, to ensure reliability and stability.
---

## 3. TDD Workflow

1. **Write a failing test** for the next bit of functionality.
2. **Write the minimum code** necessary to make the test pass.
3. **Refactor** the code for clarity and maintainability.
4. **Repeat** for each new feature or bugfix.

---

## 4. Continuous Integration

- All tests (unit and E2E) must pass in CI before merging.
- Use GitHub Actions or similar for automated testing.

---

## 5. Best Practices

- **Code Reviews:**  
  - All code must be reviewed before merging.
  - Reviewers should check for test coverage, code clarity, and adherence to this policy.

- **Documentation:**  
  - Document complex logic and public APIs.
  - Update README and architecture docs as needed.

- **Security:**  
  - Never commit secrets or credentials.
  - Use environment variables for sensitive data.

---

**By following this policy, the team ensures high code quality, reliability, and maintainability.**
