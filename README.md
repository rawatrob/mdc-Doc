# MDC Rules for Cursor IDE - Developer Guide

This guide provides detailed instructions on integrating and using MDC (Markdown Cursor) rules in your project, specifically tailored for **React** and **Node.js** developers.

---

## 🚀 Introduction

**MDC (Markdown Cursor)** rules are structured configuration files (`.mdc`) used within the Cursor IDE to control and optimize AI assistance in your development workflow. They ensure code quality, consistency, and adherence to project guidelines.

---

## 📌 Benefits of Using MDC Rules

* **Consistency:** Standardizes code practices across your entire team.
* **Efficiency:** Automates repetitive checks, reducing manual review.
* **Maintainability:** Improves codebase organization and long-term maintenance.
* **Collaboration:** Simplifies onboarding and promotes teamwork.

---

## 🛠️ Step-by-Step Integration Guide

### Step 1: Project Setup

Ensure your project's structure includes the following directories:

```sh
project-root/
├── src/
│   └── components/
├── public/
├── server/
├── package.json
└── .cursor/
    └── rules/
```

If the `.cursor/rules` directory does not exist, create it manually:

```sh
mkdir -p .cursor/rules
```

### Step 2: Create an MDC File

Within `.cursor/rules/`, create a new `.mdc` file, e.g., `react-node-guidelines.mdc`, structured as follows:

**Example:**

````yaml
---
description: Guidelines for React and Node.js projects
globs:
  - "src/components/**/*.jsx"
  - "server/**/*.js"
---

# React and Node.js Best Practices

## React Guidelines
- Always use functional components with hooks (`useState`, `useEffect`, `useRef`).
- Clearly separate UI logic from business logic.
- Components should have clear and descriptive naming conventions (e.g., `UserProfile.jsx`).

### Example:
```jsx
import React, { useState } from 'react';

const UserProfile = () => {
  const [user, setUser] = useState(null);

  useEffect(() => {
    fetchUserData().then(setUser);
  }, []);

  return user ? <div>{user.name}</div> : <div>Loading...</div>;
};

export default UserProfile;
````

## Node.js Guidelines

* Implement RESTful APIs clearly structured by resources and actions.
* Consistent error handling and clear status code responses.
* Modularize services and controllers for better readability.

### Example:

```js
// userController.js
exports.getUser = async (req, res) => {
  try {
    const user = await UserService.getUser(req.params.id);
    if (!user) return res.status(404).json({ error: 'User not found' });
    res.json(user);
  } catch (error) {
    res.status(500).json({ error: 'Internal Server Error' });
  }
};
```

### Step 3: Verify MDC Integration

Open the Cursor IDE and verify your rules:

1. Navigate to **`Settings > Rules`**.
2. Confirm the `.mdc` file is detected and applied to relevant files.

---

## 📐 MDC File Structure Overview

MDC files use a simple YAML front-matter syntax, followed by Markdown content:

```yaml
---
description: Clearly describes the rule's purpose
globs:
  - "path/to/files/**/*.ext"
---

# Markdown Instructions

- Clearly documented guidelines and standards
- Practical code examples and snippets
```

* **Description:** Explain the goal of the rule.
* **Globs:** Specify file patterns the rule applies to (supports wildcards).
* **Markdown Content:** Guidelines, code examples, and best practices.

---

## ✅ Best Practices for MDC

* Keep MDC files focused on specific standards or topics.
* Use clear and descriptive filenames.
* Regularly update rules based on project evolution.
* Ensure MDC files are part of your project's version control system.

---

## 📖 Licensing

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contribution Guidelines

Your feedback and contributions are encouraged. Please open an issue or submit a pull request with suggestions and improvements.

---

Happy Coding! 🚀✨