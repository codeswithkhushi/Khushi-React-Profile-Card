# 🪪 React Glassmorphism Profile Card — ApnoAI Task 2

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?logo=visual-studio-code&logoColor=white)
![Vercel](https://img.shields.io/badge/Deployed-Vercel-black?logo=vercel&logoColor=white)

A modern, responsive **Glassmorphism Profile Card** built with **React 18** and **Tailwind CSS**, designed entirely within a single HTML file (zero build tools or npm install needed).

Built as part of **ApnoAI Internship Task 2: Build a React Component**.

---

## 👩‍💻 Intern Profile & Tech Stack

- **Intern Name**: Khushi
- **Role**: Web Development Intern at ApnoAI
- **Status**: 🟢 Web Dev Intern @ ApnoAI
- **Internship Validity**: 🗓️ **14 Oct 2026 – 14 Nov 2026**
- **Technologies & Tools**:
  - `HTML`
  - `CSS`
  - `JavaScript`
  - `React`
  - `Git`
  - `GitHub`
  - `VS Code`
- **Official Profiles (Clickable Buttons)**:
  - [GitHub Profile](https://github.com/codeswithkhushi) (with official GitHub logo)
  - [LinkedIn Profile](https://www.linkedin.com/in/khushi-67102939a) (with official LinkedIn logo)

---

## 🌟 Key Features

1. **Modern Glassmorphism Design (2026 Standard)**
   - Translucent glass panel with `backdrop-filter: blur(24px)`.
   - Floating ambient animated gradient orbs.
   - Fully responsive on mobile, tablet, and desktop screens.

2. **Component & Props Architecture**
   - Pure React component structure (`ProfileCard`).
   - Dynamic props for `name`, `role`, `status`, `validity`, `bio`, `skills`, `avatar`, `github`, and `linkedin`.
   - List rendering via `.map()` for technology chips.

3. **Multi-State Interactivity (`useState`)**
   - 🌙 / ☀️ **Dark & Light Mode Toggle**: Smooth theme transition.
   - 🤝 **Connect Button**: Interactive connection toggle (`Connect` ↔ `✓ Connected with Khushi`).
   - ❤️ **Interactive Like Counter (+10 XP Bonus)**: Dynamic counter with animated heart icon.

4. **Dedicated GitHub & LinkedIn Buttons**
   - Clean, accessible buttons that open directly in a new tab (`target="_blank"`).

---

## 🧠 Core React Concepts Learned

### 1. Thinking in Components
React applications are composed of small, modular UI units called **Components**.

```jsx
function ProfileCard({ name, role, validity, bio, skills, avatar, github, linkedin }) {
  // Encapsulated UI markup and logic
}
```

### 2. Props vs. State

| Feature | **Props** (Inputs) | **State** (Internal Memory) |
|---|---|---|
| **What is it?** | Data passed **IN** to the component | Data managed **INSIDE** the component |
| **Mutability** | **Read-only** (Immutable) | **Mutable** via updater functions (`useState`) |
| **In this Project** | `name`, `role`, `validity`, `skills`, `github`, `linkedin` | `isDark`, `isConnected`, `likes`, `hasLiked` |

---

## 🤖 Debugging with AI: "Explain, Don't Solve"

### Experiment & Debugging Log:
1. **Scenario**: Intentionally changed `useState` to lowercase `usestate`.
2. **Error in Console**:
   ```
   Uncaught ReferenceError: usestate is not defined
   ```
3. **AI Consultation Prompt**:
   > *"Explain this React error to me like I am a beginner and tell me how to fix it: Uncaught ReferenceError: usestate is not defined"*
4. **Key Takeaway**:
   - JavaScript is case-sensitive. React hooks use camelCase (`useState`).
   - Destructuring `{ useState } = React` imports `useState`. Calling `usestate` looks for an undeclared global variable.

---

## 💻 How to Run Locally

1. Open **`index.html`** directly in any modern browser (Chrome, Edge, Firefox).
2. Or use the VS Code **Live Server** extension.

---

## 📦 Deployment Workflow

### 1. Git Push
```bash
git add .
git commit -m "feat: update technologies list and add internship validity period"
git push origin main
```

### 2. Deploy on Vercel
1. Go to [vercel.com](https://vercel.com) and log in with GitHub.
2. Click **Add New** → **Project** → Import `apnoai-task-2-khushi`.
3. Framework Preset: **Other** → Click **Deploy**.

---

## 👩‍💻 Author
- **Khushi**
- GitHub: [@codeswithkhushi](https://github.com/codeswithkhushi)
- LinkedIn: [khushi-67102939a](https://www.linkedin.com/in/khushi-67102939a)
- Internship: **ApnoAI Web Development Program**
