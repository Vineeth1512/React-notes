# 🚀 How to Install Tailwind CSS in a React Project (Vite)

This guide explains how to install and configure **Tailwind CSS** in a React project created using **Vite**.

---

# Step 1: Create a React Project

```bash
npm create vite@latest my-app
```

Choose:

- Framework: **React**
- Variant: **JavaScript** (or TypeScript)

Move into the project folder:

```bash
cd my-app
```

Install project dependencies:

```bash
npm install
```

---

# Step 2: Install Tailwind CSS

Install Tailwind CSS along with the Vite plugin:

```bash
npm install tailwindcss @tailwindcss/vite
```

---

# Step 3: Configure Vite

Open **vite.config.js** and add the Tailwind plugin.

```javascript
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";
import tailwindcss from "@tailwindcss/vite";

export default defineConfig({
  plugins: [
    react(),
    tailwindcss(),
  ],
});
```

---

# Step 4: Add Tailwind CSS

Open **src/index.css**

Remove everything and add:

```css
@import "tailwindcss";
```

---

# Step 5: Start the Development Server

```bash
npm run dev
```

---

# Step 6: Test Tailwind CSS

Open **App.jsx**

```jsx
function App() {
  return (
    <div className="flex items-center justify-center h-screen bg-blue-100">
      <h1 className="text-5xl font-bold text-blue-600">
        Tailwind CSS is Working! 🎉
      </h1>
    </div>
  );
}

export default App;
```

If the text is large, blue, and centered, Tailwind CSS is installed successfully.

---

# Folder Structure

```
my-app/
│
├── node_modules/
├── public/
├── src/
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
│
├── package.json
├── vite.config.js
└── ...
```

---

# Useful Commands

### Create React Project

```bash
npm create vite@latest my-app
```

### Install Dependencies

```bash
npm install
```

### Install Tailwind CSS

```bash
npm install tailwindcss @tailwindcss/vite
```

### Run Development Server

```bash
npm run dev
```

### Build for Production

```bash
npm run build
```

---

# Verify Installation

You can quickly test Tailwind by adding:

```jsx
<h1 className="text-4xl font-bold text-red-500">
  Hello Tailwind!
</h1>
```

Expected output:

- ✅ Large text
- ✅ Bold font
- ✅ Red color

---

# Common Issues

## 1. Styles Not Applying

- Ensure `@import "tailwindcss";` exists in `src/index.css`.
- Restart the development server.

---

## 2. Plugin Not Working

Check that **vite.config.js** includes:

```javascript
import tailwindcss from "@tailwindcss/vite";
```

and

```javascript
plugins: [
  react(),
  tailwindcss(),
];
```

---

## 3. Forgot to Restart

After changing the Vite configuration:

```bash
Ctrl + C
npm run dev
```

Restart the server.

---

# Congratulations! 🎉

Your React + Vite project is now ready to use Tailwind CSS.

Example:

```jsx
<button className="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">
  Click Me
</button>
```
