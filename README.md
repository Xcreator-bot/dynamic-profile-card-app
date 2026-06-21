# Dynamic Profile Card App

A small React app for managing a list of user profiles — follow/unfollow users, search by name, and toggle between light and dark themes. Built to practice core React fundamentals: **props** for passing data down, and **state** for managing data that changes over time.

🔗 **[Live Demo](https://xcreator-bot.github.io/dynamic-profile-card-app/)** 

![App Screenshot](./assets/screenshot.png)

---

## Features

- 🧑‍🤝‍🧑 Profile cards rendered from a single array of user data
- ➕ Follow / Unfollow toggle on each card, with live UI updates
- 🌓 Global Dark / Light mode switch
- 🔍 Live search filter by name
- 🪝 `useEffect` hook logging follow changes to the console

## Tech Stack

- **React 18** (loaded via CDN, no build step)
- **Babel Standalone** for in-browser JSX compilation
- Plain CSS with CSS custom properties for theming

No npm install, no bundler, no build step — clone it and open `index.html`.

---

## Getting Started

```bash
git clone https://github.com/<your-username>/dynamic-profile-card-app.git
cd dynamic-profile-card-app
```

Then just open `index.html` in your browser. That's it.

> Requires an internet connection on first load, since React, ReactDOM, and Babel are loaded from a CDN rather than bundled locally.

---

## Project Structure

```
dynamic-profile-card-app/
├── index.html      # the complete, runnable app
├── app.jsx          # component logic (same code as index.html, kept separate for readability)
├── styles.css        # theme & layout styles (same code as index.html, kept separate for readability)
├── assets/
│   └── screenshot.png
└── README.md
```

> **Note:** `app.jsx` and `styles.css` are reference copies for easy reading — the actual app in `index.html` is self-contained and includes this same code inline.

---

## What I Practiced

This project was built to get hands-on with two of React's core concepts:

- **Props** — `ProfileCard` is a reusable, read-only component. It receives `name`, `bio`, `avatar`, and `isFollowed` from its parent and never modifies them directly.
- **State** — `App` owns all the data that changes over time: the list of profiles, the active theme, and the search text. All updates go through `useState` setter functions, never direct mutation — for example, toggling follow status rebuilds the profiles array with `.map()` instead of mutating an object in place.
- **Lifting state up** — theme and search state live in the parent so they can control every child card at once.
- **useEffect** — runs a side effect (logging to console) only when the `profiles` state actually changes, demonstrating dependency arrays.

## Possible Improvements

- Persist follow state and theme preference with localStorage
- Add unit tests (Jest + React Testing Library)
- Migrate to a bundler (Vite) for a production build and code splitting
- Add pagination or infinite scroll for larger user lists

---

## Author

**Ammara Majeed**
Frontend Developer Intern — Appverse Technologies

