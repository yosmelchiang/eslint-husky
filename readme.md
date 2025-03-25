### 1. **Install Husky**

```bash
npm install husky
```

### 2. **Enable Git Hooks**

The init command simplifies setting up husky in a project. It creates a `pre-commit` script in `.husky/` and updates the `prepare` script in `package.json`.

```bash
npx husky init
```

- Creates a `.husky` directory in project root.
- The `.husky` directory will store all the Git hooks that Husky manages, such as `pre-commit`.

- Check that a prepare script is added to `package.json`.

```json
{
  "scripts": {
    "prepare": "husky install"
  }
}
```

### 3. **Create Pre-commit Hook**

Create a pre-commit hook that runs linting (or any other task) before commits are made. For example, to run ESLint before each commit, add this pre-commit hook:

```bash
npx eslint
```

- Replace `npx eslint` with any other command (e.g., running tests or formatting).

---

### Summary

Here’s a recap of the commands:

1. Install Husky:

   ```bash
   npm install husky
   ```

2. Initialize Husky:

   ```bash
   npx husky init
   ```

3. Look for the `prepare` script to `package.json` (so Husky uses the hooks automatically):

   ```json
   "scripts": {
     "prepare": "husky"
   }
   ```

4. Create the pre-commit hook:

   ```bash
   npx eslint
   ```

5. If necessary, set up ESLint:
- [ESLINT example](https://github.com/yosmelchiang/eslint-example)


---
