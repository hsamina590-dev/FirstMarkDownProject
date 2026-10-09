# Tailwind CSS Practice

## Dark Mode

Dark mode allows users to view a website with dark backgrounds and light text. It provides an alternative appearance for websites and dashboards.

---

<details>
<summary>01 — Understand Dark Mode</summary>

### Code

```tsx
<div className="bg-white p-6 text-gray-900">
  <h2 className="text-2xl font-bold">Light Mode</h2>
  <p>This is a light theme.</p>
</div>

<div className="bg-gray-900 p-6 text-white">
  <h2 className="text-2xl font-bold">Dark Mode</h2>
  <p>This is a dark theme.</p>
</div>
```

### Tailwind Class

`bg-white` · `text-gray-900` · `bg-gray-900` · `text-white`

### ↓ We Learn

Light mode uses light backgrounds and dark text. Dark mode uses dark backgrounds and light text.

</details>

---

<details>
<summary>02 — Configure Dark Mode</summary>

### Code

Add the following configuration to `src/app/globals.css` when using Tailwind CSS v4 with class-based dark mode:

```css
@import "tailwindcss";

@custom-variant dark (&:where(.dark, .dark *));
```

### Tailwind Class

`@custom-variant dark`

### ↓ We Learn

This configuration allows `dark:` utilities to apply when an element is inside an element with the `dark` class.

</details>

---

<details>
<summary>03 — Use dark:</summary>

### Code

```tsx
<div className="bg-white p-6 text-black dark:bg-gray-900 dark:text-white">
  <h2 className="text-xl font-bold">Welcome</h2>
  <p>This content supports dark mode.</p>
</div>
```

### Tailwind Class

`dark:bg-gray-900` · `dark:text-white`

### ↓ We Learn

The `dark:` variant allows us to define different styles for dark mode.

</details>

---

<details>
<summary>04 — Dark Backgrounds</summary>

### Code

```tsx
<div className="bg-gray-100 p-6 dark:bg-gray-950">
  <h2 className="text-xl font-bold">Dark Background</h2>
  <p className="mt-2">The background changes with the theme.</p>
</div>
```

### Tailwind Class

`bg-gray-100` · `dark:bg-gray-950`

### ↓ We Learn

The background appears light gray in light mode and almost black in dark mode.

</details>

---

<details>
<summary>05 — Dark Text</summary>

### Code

```tsx
<p className="text-gray-800 dark:text-gray-200">
  This text is readable in both themes.
</p>
```

### Tailwind Class

`text-gray-800` · `dark:text-gray-200`

### ↓ We Learn

We use dark text in light mode and light text in dark mode to keep the content readable.

</details>

---

<details>
<summary>06 — Dark Borders</summary>

### Code

```tsx
<div className="rounded-lg border border-gray-300 p-4 dark:border-gray-700">
  <h2 className="font-bold">Border Example</h2>
  <p className="mt-2">The border changes with the theme.</p>
</div>
```

### Tailwind Class

`border-gray-300` · `dark:border-gray-700`

### ↓ We Learn

We change the border color in dark mode to maintain a consistent appearance with the background.

</details>

---

<details>
<summary>07 — Dark Cards</summary>

### Code

```tsx
<div className="rounded-xl bg-white p-6 shadow-lg dark:bg-gray-800">
  <h2 className="text-xl font-bold text-gray-900 dark:text-white">
    Product Card
  </h2>

  <p className="mt-2 text-gray-600 dark:text-gray-300">
    This card supports both themes.
  </p>

  <button className="mt-4 rounded-lg bg-blue-600 px-4 py-2 text-white">
    View Product
  </button>
</div>
```

### Tailwind Class

`bg-white` · `dark:bg-gray-800` · `dark:text-white`

### ↓ We Learn

We can style card backgrounds, text, and shadows to match the selected theme.

</details>

---

<details>
<summary>08 — Dark Forms</summary>

### Code

```tsx
<form className="space-y-4 rounded-xl bg-white p-6 dark:bg-gray-800">
  <label className="block font-medium text-gray-900 dark:text-white">
    Email
  </label>

  <input
    type="email"
    placeholder="Enter your email"
    className="w-full rounded-lg border border-gray-300 bg-white p-3 text-gray-900 placeholder:text-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-500 dark:border-gray-600 dark:bg-gray-900 dark:text-white dark:placeholder:text-gray-500"
  />

  <button className="rounded-lg bg-blue-600 px-5 py-2 text-white">
    Submit
  </button>
</form>
```

### Tailwind Class

`dark:bg-gray-900` · `dark:text-white` · `dark:border-gray-600`

### ↓ We Learn

We style form fields with different backgrounds, borders, and text colors for dark mode.

</details>

---

<details>
<summary>09 — Dark Navigation</summary>

### Code

```tsx
<nav className="flex items-center justify-between bg-white p-4 shadow dark:bg-gray-900">
  <h1 className="text-xl font-bold text-gray-900 dark:text-white">
    MyWebsite
  </h1>

  <div className="flex gap-4">
    <a
      className="text-gray-700 hover:text-blue-600 dark:text-gray-200 dark:hover:text-blue-400"
      href="#"
    >
      Home
    </a>

    <a
      className="text-gray-700 hover:text-blue-600 dark:text-gray-200 dark:hover:text-blue-400"
      href="#"
    >
      About
    </a>
  </div>
</nav>
```

### Tailwind Class

`dark:bg-gray-900` · `dark:text-white` · `dark:hover:text-blue-400`

### ↓ We Learn

We adjust the navigation bar background, link colors, and hover colors for dark mode.

</details>

---

<details>
<summary>10 — Dark Dashboards</summary>

### Code

```tsx
<div className="min-h-screen bg-gray-100 p-6 dark:bg-gray-950">
  <h1 className="mb-6 text-2xl font-bold text-gray-900 dark:text-white">
    Dashboard
  </h1>

  <div className="grid grid-cols-1 gap-4 md:grid-cols-3">
    <div className="rounded-xl bg-white p-5 shadow dark:bg-gray-800">
      <p className="text-gray-500 dark:text-gray-300">Users</p>
      <h2 className="mt-2 text-3xl font-bold text-gray-900 dark:text-white">
        120
      </h2>
    </div>

    <div className="rounded-xl bg-white p-5 shadow dark:bg-gray-800">
      <p className="text-gray-500 dark:text-gray-300">Orders</p>
      <h2 className="mt-2 text-3xl font-bold text-gray-900 dark:text-white">
        85
      </h2>
    </div>

    <div className="rounded-xl bg-white p-5 shadow dark:bg-gray-800">
      <p className="text-gray-500 dark:text-gray-300">Revenue</p>
      <h2 className="mt-2 text-3xl font-bold text-gray-900 dark:text-white">
        $500
      </h2>
    </div>
  </div>
</div>
```

### Tailwind Class

`min-h-screen` · `grid` · `md:grid-cols-3` · `dark:bg-gray-950` · `dark:bg-gray-800`

### ↓ We Learn

Dashboard cards and page backgrounds can support both themes. Responsive grids arrange cards for different screen sizes.

</details>

---

<details>
<summary>11 — Light/Dark Color Consistency</summary>

### Code

```tsx
<div className="rounded-xl border border-gray-200 bg-white p-6 text-gray-900 dark:border-gray-700 dark:bg-gray-900 dark:text-white">
  <h2 className="text-xl font-bold">Consistent Design</h2>

  <p className="mt-2 text-gray-600 dark:text-gray-300">
    Text and background colors remain readable in both themes.
  </p>

  <button className="mt-4 rounded-lg bg-blue-600 px-4 py-2 text-white hover:bg-blue-700">
    Continue
  </button>
</div>
```

### Tailwind Class

`bg-white` · `dark:bg-gray-900` · `text-gray-900` · `dark:text-white`

### ↓ We Learn

We maintain consistent color contrast so that text, borders, and buttons remain readable in both light and dark themes.

</details>

---

<details>
<summary>12 — Build: Light/Dark Dashboard</summary>

### Code

Add this example to `src/app/page.tsx` in your Next.js project. If your project does not have a `src` folder, use `app/page.tsx`.

```tsx
"use client";

import { useState } from "react";

export default function Home() {
  const [darkMode, setDarkMode] = useState(false);

  return (
    <main className={darkMode ? "dark" : ""}>
      <div className="min-h-screen bg-gray-100 p-6 text-gray-900 transition-colors duration-300 dark:bg-gray-950 dark:text-white">

        <nav className="mb-8 flex flex-wrap items-center justify-between gap-4">
          <h1 className="text-2xl font-bold">
            My Dashboard
          </h1>

          <button
            type="button"
            onClick={() => setDarkMode(!darkMode)}
            className="rounded-lg bg-blue-600 px-4 py-2 text-white transition-colors hover:bg-blue-700"
          >
            {darkMode ? "☀️ Light Mode" : "🌙 Dark Mode"}
          </button>
        </nav>

        <p className="mb-6 text-gray-600 dark:text-gray-300">
          Welcome back! Here is your dashboard overview.
        </p>

        <div className="grid grid-cols-1 gap-5 sm:grid-cols-2 lg:grid-cols-3">

          <div className="rounded-xl border border-gray-200 bg-white p-6 shadow-sm dark:border-gray-700 dark:bg-gray-800">
            <p className="text-gray-500 dark:text-gray-300">
              Total Users
            </p>
            <h2 className="mt-2 text-3xl font-bold">
              1,250
            </h2>
          </div>

          <div className="rounded-xl border border-gray-200 bg-white p-6 shadow-sm dark:border-gray-700 dark:bg-gray-800">
            <p className="text-gray-500 dark:text-gray-300">
              Total Orders
            </p>
            <h2 className="mt-2 text-3xl font-bold">
              860
            </h2>
          </div>

          <div className="rounded-xl border border-gray-200 bg-white p-6 shadow-sm dark:border-gray-700 dark:bg-gray-800">
            <p className="text-gray-500 dark:text-gray-300">
              Total Revenue
            </p>
            <h2 className="mt-2 text-3xl font-bold">
              $4,500
            </h2>
          </div>

        </div>

        <section className="mt-8 rounded-xl border border-gray-200 bg-white p-6 dark:border-gray-700 dark:bg-gray-800">
          <h2 className="text-xl font-bold">
            Recent Activity
          </h2>

          <p className="mt-2 text-gray-600 dark:text-gray-300">
            Your latest dashboard updates appear here.
          </p>
        </section>

      </div>
    </main>
  );
}
```

### Tailwind Class

`dark:` · `bg-gray-100` · `dark:bg-gray-950` · `dark:bg-gray-800` · `dark:text-white` · `transition-colors` · `duration-300`

### ↓ We Learn

* `useState` stores the current light or dark mode state.
* Clicking the button switches between themes.
* `dark:` utilities apply the dark theme colors.
* `transition-colors` makes color changes smooth.
* Responsive grid classes arrange dashboard cards on different screen sizes.

### Build

**A dashboard supporting both light and dark themes.**

</details>

### Important: 
 The first 11 sections demonstrate individual dark-mode concepts. The final Build section creates a working dashboard with a button that switches between light and dark themes.
