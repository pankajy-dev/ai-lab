# User Prompts Log

This file contains a sequential list of all prompts given by the user to the system. New prompts will be appended as they are provided.

## Chapter 1 - Designing  application

---
---

### 1. [Initial Prompt]
I'm building a cooking receipe sharing application that people register their own recipes and share with other users. Use Next.js and Material UI (UI) for frontend, Supabase for DB + auth.

Give me the full architecture:
- File + folder structure
- What each part does
- Where state lives, how services connect

Format this entire document in markdown.

---

### 2. Save the previous plan
save this document as a markdown as .clinerules/01_architecture.md

---

### 3. Creating coding policy
Add .clinerules/02_coding_policy.md for code practice in this project. I'd like to follow TDD approach and have unit tests and E2Es.

---

### 4. Creating a task list
Using that @/.clinerules/01_architecture.md and @/.clinerules/02_coding_policy.md , write a granular step-by-step plan to build the MVP. 

Each task should: 
- Be incredibly small + testable
- Have a clear start + end
- Focus on one concern 

I'll be passing this off to an engineering LLM that will be told to complete one task at a time, allowing me to test in between. 

---

### 5. Save the task list
Save the task list as task.md at the repository root.

---
---

## Chapter 2 - Bootstrapping application

---
---

### 1 Bootstrap a new application
You're an engineer building this codebase.

You've been given .clinerules/01_architecture.md and task.md

- Read both carefully. There should be no ambiguity about what we're building.
- Follow tasks.md and complete one task at a time.
- After each task, stop. I'll test it. If it works, commit to git and move to the next.


### CODING PROTOCOL ###
Read .clinerules/02_coding_policy.md as Coding Instructions

---

### 2 Update tasks.md
Please update tasks.md to clarify which tasks we completed.

---

### 3 Add technology_stack document
```markdown
Add a new cline rule called "03_technology_stack" and clarify we want to use


# Programming language
- TypeScript

# Web application framework
- Next.js
- React

# CSS framework
- Material UI

# Frontend state management
- Zustand
```

---

### 4 Configure formatter
```
Configure prittier and use prittier format with `npm run format`
```

---

### 5 Install dependencies
```
move on to the next task
```

---

### 6 Updating codiny policy
```
Update coding_policy clien rule to add the following policy

- we always check `npx playwright test` passes without error. If there are errors. 
- We have to take a look at code changes and fix and rerun tests. 
- This loop must be executed at least 3 times if we have test failures.
```
---

### 6.1
```
Update tasks.md to complete the task.
```
---

### 7 Setup typescript
```
Move on to the next task.
```

---
---

## Chapter 3 - Integrating Supabase

---
---

### 1 Sign-up
```
Move on to the next task.
```

---

### 2  Update task
```
Update task.md to complete the task
```

---

### 3 Set up env variables after getting url and keys from supabase

```
Use following project URL and ANON key

Project URL: https://dybhxmhsqapakspnuyjc.supabase.co
ANON key: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImR5Ymh4bWhzcWFwYWtzcG51eWpjIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NDkwMTU1ODYsImV4cCI6MjA2NDU5MTU4Nn0.EwoAFmGWe4L9ylQj6OYfujZEZChUb9IDeciBmndmHug
```

### 3.1 
```
Update tasks.md to complete the task.
```

---

### 3-3 Configure Supabase client
```
Move on to next task
```


