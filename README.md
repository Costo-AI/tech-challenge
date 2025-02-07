# **Intern Tech Challenge: React & TypeScript**
Welcome to the **Full-Stack Intern Tech Challenge**! 🎉  
This challenge will test your ability to work with **React, TypeScript, and API fetching** while implementing client-side filtering.

---

## **📌 Challenge Overview**
Your task is to **build a React application** that:  
✅ Lists posts from an API.  
✅ Includes a **search bar** to filter posts by title.  
✅ Includes a **dropdown** to filter posts by the author (users).  
✅ Uses **TypeScript** to ensure type safety.  
✅ Implements **good UI state management**.

---

## **📌 API Information**
We have provided a **mock API** that contains:

### **1️⃣ Users (Authors)**
📌 Endpoint: [`/users`](https://my-json-server.typicode.com/Costo-AI/intern-tech-challenge/users)

### **2️⃣ Posts**
📌 Endpoint: [`/posts`](https://my-json-server.typicode.com/Costo-AI/intern-tech-challenge/posts)

### **Example Data Structure**
#### **📍 User**
```json
{
  "id": 1,
  "name": "Alice Johnson",
  "email": "alice@example.com"
}
```
#### **📍 Post**
```json
{
  "id": 1,
  "title": "React Performance Tips",
  "body": "Optimize re-renders and use memoization.",
  "userId": 1
}
```
You can find the list of available endpoints: https://my-json-server.typicode.com/Costo-AI/intern-tech-challenge

- Users: https://my-json-server.typicode.com/Costo-AI/intern-tech-challenge/users
- Posts: https://my-json-server.typicode.com/Costo-AI/intern-tech-challenge/posts

---

## **📌 Setup Instructions**

### **1️⃣ Clone the repository**
```bash
git clone https://github.com/Costo-AI/intern-tech-challenge.git
cd intern-tech-challenge
```

### **2️⃣ Install dependencies**

```bash
npm install
```

### **3️⃣ Start the development server**
```bash
npm run dev
```

## **📌 Requirements**

### **1️⃣ Display a List of Posts**
- Fetch posts from the API
- Display title and body of each post.

### **2️⃣ Add a Search Filter**
- Implement a search input field
- Filter posts by title (client-side).

### **3️⃣ Add a Dropdown to Filter by User**
- Fetch the users from the API
- Display a dropdown with the users’ names
- Allow filtering posts by selected user

### **4️⃣ Ensure Type Safety**
- Define TypeScript types for:
    - Post
    - User
    - Use useState and useEffect correctly.

---

### **📌 Bonus Features (Optional)**
💡 Debounce the search input (e.g., delay filtering)  
💡 Show a loading spinner when fetching data.  
💡 Implement sorting (e.g., order posts alphabetically).  
💡 Use React Context for state management.

---

## **📌 Submission Instructions**

### **1. Create a new branch with your name.**
### **2.	Commit your changes.**
### **3.	Push to GitHub.**

---

## **📌 Evaluation Criteria**

✅ Correctness: Does the app meet the requirements?  
✅ Code Quality: Is the code well-structured and readable?  
✅ Type Safety: Are TypeScript types used properly?  
✅ Performance: Are unnecessary re-renders avoided?  
✅ UX & UI: Is the app user-friendly?

💡 Need help? Feel free to ask us questions if anything is unclear.  
Good luck, and have fun coding! 🚀😃

---


# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default tseslint.config({
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

- Replace `tseslint.configs.recommended` to `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`
- Optionally add `...tseslint.configs.stylisticTypeChecked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and update the config:

```js
// eslint.config.js
import react from 'eslint-plugin-react'

export default tseslint.config({
  // Set the react version
  settings: { react: { version: '18.3' } },
  plugins: {
    // Add the react plugin
    react,
  },
  rules: {
    // other rules...
    // Enable its recommended rules
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
})
```
