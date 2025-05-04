# MDC Rules for Cursor IDE

This repository contains MDC (Markdown Cursor) rules designed to enhance your development workflow, specifically tailored for projects using **React** and **Node.js**.

---

## 🚀 What is MDC?

**MDC (Markdown Cursor)** rules are configuration files (`.mdc`) used by the Cursor IDE to guide its AI assistant behavior. They ensure your codebase consistently follows predefined guidelines, best practices, and coding standards.

MDC files help:

* Enforce coding conventions
* Automate common tasks
* Maintain consistent project structure
* Enhance team collaboration

---

## 📌 Why Use MDC?

Using MDC rules in your Cursor IDE-powered projects offers:

* **Consistency:** Ensure the entire team adheres to the same coding conventions.
* **Efficiency:** Automate routine checks, reducing manual review time.
* **Maintainability:** Easier maintenance and scalability of your codebase.
* **Improved Collaboration:** Simplify onboarding and reduce friction in collaborative environments.

---

## ⚙️ How to Add MDC to Your Project

Follow these easy steps to integrate MDC rules into your project:

### Step 1: Setup

Create the following directory structure in your project root:

```sh
project-root/
├── src/
│   └── components/
├── public/
├── package.json
└── .cursor/
    └── rules/
```

### Step 2: Create MDC Files

Place `.mdc` files inside the `.cursor/rules/` directory.

**Example file:** `react-node-guidelines.mdc`

```yaml
---
description: Guidelines for React and Node.js projects
globs:
  - "src/components/**/*.jsx"
  - "server/**/*.js"
---

# React and Node.js Best Practices

- Use React functional components with hooks (useState, useEffect, useRef).
- Clearly separate client-side and server-side logic.
- Maintain consistent naming conventions for components and server modules.
- Follow RESTful principles and maintain clear API endpoints in Node.js.
- Ensure comprehensive error handling in both React components and Node.js services.
```

### Step 3: Verify Integration

Open the Cursor IDE, navigate to `Settings > Rules`, and confirm your MDC rules are correctly detected and applied.

---

## 📐 MDC File Structure

MDC rules follow a structured format:

```yaml
---
description: Brief description of the rule
globs:
  - "path/to/files/**/pattern*.ext"
---

# Markdown Content

- Detailed guidelines, best practices, or coding conventions.
- Example code snippets.
```

### Explanation:

* **Description:** Clearly explains what the rule achieves.
* **Globs:** Specifies which files the rule applies to (supports wildcards).
* **Markdown Content:** Includes detailed guidelines and code snippets illustrating the intended coding standards.

---

## ✅ Best Practices

* Keep MDC rules specific and focused.
* Name MDC files clearly and descriptively.
* Regularly review and update MDC rules as the project evolves.
* Include MDC rules in your project's version control system.

---

## 📖 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🤝 Contribution

Contributions, feedback, and suggestions are welcome. Feel free to open an issue or submit a pull request.

---

Happy Coding! 🚀✨
