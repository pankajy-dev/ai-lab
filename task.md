# MVP Build Plan – Cooking Recipe Sharing App

This file contains a granular, step-by-step plan to build the MVP, based on the architecture and coding policy.  
**Complete one task at a time. After each task, stop for testing/approval before moving to the next.**

---

## 1. Project Initialization & Tooling

1. **Initialize Next.js App with TypeScript**
   - [x] Scaffold a new Next.js app in `recipe-app/` with TypeScript.
   - [x] Add a basic README.
   - [x] Write a test to check the app renders the home page.

2. **Set Up Linting, Formatting, and Pre-commit Hooks**
   - [x] Add ESLint, Prettier, and configure rules.
   - [x] Set up Husky or lint-staged for pre-commit checks.
   - [x] Add a test to ensure linting passes on a sample file.

3. **Install and Configure Material UI**
   - [x] Install Material UI and set up a custom theme in `src/theme/`.
   - [x] Add a test to check a Material UI component renders.

4. **Install and Configure Supabase**
   - [x] Install Supabase JS client.
   - [x] Create `src/services/supabaseClient.ts` and connect to Supabase.
   - [x] Add a test to check Supabase client initializes with env vars.

   - [x] Supabase Project URL and ANON key have been configured in `.env.local` as per best practices. The client is now fully set up and ready for use.

---

## 2. Project Structure & Boilerplate

5. **Create Folder Structure**
   - [x] Create all folders as per architecture: `components/`, `features/`, `layouts/`, `theme/`, `utils/`, `hooks/`, `services/`, `types/`.
   - [x] Add placeholder files (e.g., `index.ts`) in each.
   - [x] Add a test to check folder structure exists.

6. **Set Up Global Providers**
   - [x] Implement `_app.tsx` with ThemeProvider and AuthProvider.
   - [x] Add a test to check providers wrap the app.

---

## 3. Authentication

7. **Implement Auth Context and Hooks**
   - [x] Create `features/auth/hooks/useAuth.ts` and AuthProvider.
   - [x] Add a test for auth context default state.

8. **Build Auth Pages (Login/Register)**
   - [x] Create `pages/auth/login.tsx` and `pages/auth/register.tsx` with Material UI forms.
   - [x] Add tests for form rendering and validation.

9. **Integrate Supabase Auth**
   - [x] Connect forms to Supabase Auth (sign up, sign in).
   - [x] Add tests for successful and failed login/register flows (mock Supabase).

---

## 4. Recipe Feature

10. **Define Recipe Types**
    - [x] Create `features/recipes/types.ts` for recipe interfaces.
    - [x] Add a test to check type usage.

11. **Recipe CRUD Services**
    - [x] Implement `features/recipes/services.ts` for CRUD operations with Supabase.
    - [x] Add unit tests for each service (mock Supabase).

12. **Recipe List Page**
    - [x] Create `pages/recipes/index.tsx` to list all recipes.
    - [x] Add a test to check recipes render from mock data.

13. **Recipe Detail Page**
    - [x] Create `pages/recipes/[id].tsx` to show a single recipe.
    - [x] Add a test for detail rendering.

14. **Recipe Form Component**
    - [x] Build `components/RecipeForm.tsx` for adding/editing recipes.
    - [x] Add tests for form validation and submission.

15. **Connect Recipe Form to Services**
    - [x] Wire up form to create/edit recipes via Supabase.
    - [x] Add tests for create/edit flows (mock Supabase).

---

## 5. User Profile

16. **User Profile Page**
    - [x] Create `pages/profile.tsx` to show user info and their recipes.
    - [x] Add a test for profile rendering.

- [x] 17. **User Services and Types**
    - Implement `features/user/services.ts` and `types.ts`.
    - Add tests for user data fetching.

---

## 6. E2E & Finalization

18. **Set Up E2E Testing**
    - [x] Install and configure Cypress or Playwright.
    - [x] Add E2E tests for registration, login, recipe CRUD, and sharing.

19. **Security & Environment**
    - [x] Ensure `.env.local` is used for all secrets.
    - [x] Add a test to check env vars are loaded.

20. **Documentation**
    - [x] Update README with setup, architecture, and coding policy.
    - [x] Add a test to check README exists.

---

**How to Use:**  
- Complete one task at a time, in order.
- After each task, stop for testing/approval before moving to the next.
- Each task should include TDD: write a failing test, implement, refactor, and ensure the test passes.

---

## Coding Policy Update Log

- [x] Updated `.clinerules/02_coding_policy.md` to include the Playwright E2E test loop policy: Always check that `npx playwright test` passes without error; if there are errors, review code changes, fix, and rerun tests; this fix-and-rerun loop must be executed at least 3 times if there are test failures.
