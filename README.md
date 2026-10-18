# 🪪 React Glassmorphism Profile Card — ApnoAI Task 2

![React 18](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.x-38B2AC?logo=tailwind-css&logoColor=white)
![Vercel](https://img.shields.io/badge/Deployed-Vercel-black?logo=vercel&logoColor=white)
![Single File](https://img.shields.io/badge/Setup-Zero_Build_Tools-success)

A modern, responsive **Glassmorphism Profile Card** built with **React 18** and **Tailwind CSS**, designed entirely within a single, lightweight HTML file (zero build tools or `npm install` needed). 

Built as part of **ApnoAI Internship Task 2: Build a React Component**.

---

## 🚀 Live Demo & Repository
- **Live Vercel URL**: *`https://apnoai-task-2-khushi.vercel.app`* *(Update with your deployed link)*
- **GitHub Repository**: [https://github.com/codeswithkhushi/apnoai-task-2-khushi](https://github.com/codeswithkhushi/apnoai-task-2-khushi)

---

## 🌟 Key Features

1. **Modern Glassmorphism UI (2026 Design Standard)**
   - Translucent glass panels with `backdrop-filter: blur(24px)`.
   - Subtle borders, floating ambient gradient orbs, and soft drop shadows.
   - Fully responsive on mobile, tablet, and desktop screens.

2. **Component & Props Architecture**
   - Pure React component structure (`ProfileCard`).
   - Dynamic props for `name`, `role`, `status`, `bio`, `skills`, `avatar`, and social links.
   - List rendering via `.map()` for skill chips.

3. **Multi-State Interactivity (`useState`)**
   - 🌙 / ☀️ **Dark & Light Mode Toggle**: Smooth theme transition across the entire page and card surfaces.
   - 🤝 **Connect Button**: Toggles connection status with feedback and state persistence (`Connect` ↔ `✓ Connected`).
   - ❤️ **Bonus Interactive Like Counter (+10 XP)**: Dynamic like button that tracks state (`likes`, `hasLiked`), incrementing and decrementing with lively heart animations.

4. **Robust Image Fallback**
   - Includes automatic `onError` image handling to ensure a smooth profile avatar display even if a link is unreachable.

5. **Extended Social Presence**
   - Direct clickable icon links for GitHub, LinkedIn, Twitter/X, and Instagram.

---

## 🧠 Core React Concepts Learned

### 1. Thinking in Components
React encourages breaking user interfaces into reusable, self-contained pieces called **Components**. Instead of maintaining one massive imperative HTML script, components encapsulate their own markup, styling, and state logic.

```jsx
function ProfileCard({ name, role, bio, skills, avatar }) {
  // Component logic and JSX markup
}
```

### 2. Props vs. State

| Feature | **Props** (Properties) | **State** (Internal Memory) |
|---|---|---|
| **What is it?** | Data passed **IN** from the parent | Data created and managed **INSIDE** |
| **Mutability** | **Read-only** (Immutable) | **Mutable** via updater functions |
| **Purpose** | Configures and personalizes components | Drives interactive, dynamic UI changes |
| **In this Project** | `name`, `role`, `bio`, `skills`, `avatar` | `isDark`, `isConnected`, `likes`, `hasLiked` |

#### State Example (`useState`):
```jsx
// 1. Theme State
const [isDark, setIsDark] = useState(false);
const toggleTheme = () => setIsDark(prev => !prev);

// 2. Bonus Interactive Counter State
const [likes, setLikes] = useState(initialLikes);
const [hasLiked, setHasLiked] = useState(false);
const handleLike = () => {
  setLikes(prev => hasLiked ? prev - 1 : prev + 1);
  setHasLiked(prev => !prev);
};
```

---

## 🤖 Debugging with AI: "Explain, Don't Solve"

As part of modern software engineering best practices, AI was utilized as a mentor to **explain underlying error mechanisms** rather than blindly generating fixes.

### Experiment & Debugging Log:
1. **Scenario**: Intentionally modified the React Hook invocation from `useState(false)` to `usestate(false)` or omitted a closing JSX tag.
2. **Error in Console**:
   ```
   Uncaught ReferenceError: usestate is not defined
   ```
3. **AI Consultation Prompt**:
   > *"Explain this React error to me like I am a beginner and tell me how to fix it: Uncaught ReferenceError: usestate is not defined"*
4. **Key Takeaway**:
   - JavaScript is strictly case-sensitive.
   - React hooks follow the camelCase naming convention (`use` prefix + capitalized hook name like `useState`, `useEffect`).
   - Destructuring `{ useState } = React` imports the exact identifier `useState`. Writing lowercase `usestate` causes the engine to look for an undeclared global variable.

---

## 💻 How to Run Locally

Because this project uses React 18 via CDN and Babel in-browser transformation, **no Node.js or npm installation is required**:

1. Clone or download this repository:
   ```bash
   git clone https://github.com/codeswithkhushi/apnoai-task-2-khushi.git
   ```
2. Navigate into the folder:
   ```bash
   cd apnoai-task-2-khushi
   ```
3. Open `index.html` directly in any web browser (Chrome, Edge, Firefox, Safari) or use the VS Code "Live Server" extension.

---

## 📦 Deployment Workflow

### 1. Git & GitHub
```bash
git init
git add index.html README.md
git commit -m "feat: add profile card component with props and state"
git branch -M main
git remote add origin https://github.com/codeswithkhushi/apnoai-task-2-khushi.git
git push -u origin main
```

### 2. Vercel Deployment
1. Log in to [Vercel](https://vercel.com) using your GitHub account.
2. Click **Add New** → **Project**.
3. Import `apnoai-task-2-khushi`.
4. Framework Preset: **Other** (static single-file deployment).
5. Click **Deploy** — your live URL will be ready in seconds!

---

## 👩‍💻 Author
- **Khushi**
- GitHub: [@codeswithkhushi](https://github.com/codeswithkhushi)
- Internship: **ApnoAI Web Development & Data Analytics Program**
