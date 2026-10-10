# UI.15 — Tailwind CSS + Next.js

Tailwind CSS with Next.js helps us build modern, responsive, and professional web applications. Next.js App Router uses folders and files to organize pages, layouts, loading screens, error screens, and other UI components.

---

<details>
<summary>01 — Tailwind CSS with Next.js</summary>

### Code

**File:** `app/page.tsx`

```tsx
export default function Home() {
  return (
    <main className="min-h-screen bg-gray-100 p-8">
      <h1 className="text-3xl font-bold text-blue-600">
        Welcome to Next.js
      </h1>

      <p className="mt-4 text-gray-600">
        Tailwind CSS makes styling easy.
      </p>

      <button className="mt-6 rounded-lg bg-blue-600 px-5 py-2 text-white hover:bg-blue-700">
        Get Started
      </button>
    </main>
  );
}
```

### Tailwind Classes

- `min-h-screen` → Full screen minimum height.
- `bg-gray-100` → Light gray background.
- `p-8` → Padding on all sides.
- `text-3xl` → Large text.
- `font-bold` → Bold text.
- `text-blue-600` → Blue text.
- `mt-4` → Top margin.
- `rounded-lg` → Rounded corners.
- `hover:bg-blue-700` → Changes background on hover.

### We Learned

- How to use Tailwind CSS inside a Next.js component.
- How to style headings, paragraphs, and buttons.
- How to create a simple responsive-friendly page.

</details>

---

<details>
<summary>02 — App Router Styling</summary>

### Code

**File:** `app/layout.tsx`

```tsx
import type { Metadata } from "next";
import "./globals.css";

export const metadata: Metadata = {
  title: "My Next.js App",
  description: "A Tailwind CSS practice project",
};

export default function RootLayout({
  children,
}: Readonly<{
  children: React.ReactNode;
}>) {
  return (
    <html lang="en">
      <body className="min-h-screen bg-slate-50 text-slate-900">
        {children}
      </body>
    </html>
  );
}
```

### Tailwind Classes

- `min-h-screen` → At least full screen height.
- `bg-slate-50` → Light background for the application.
- `text-slate-900` → Dark text color.

### We Learned

- The `app` folder contains our App Router pages and layouts.
- `layout.tsx` provides a shared structure around pages.
- `globals.css` contains global CSS and Tailwind setup.
- `metadata` defines the page title and description.

</details>

---

<details>
<summary>03 — Server Component Styling</summary>

### Code

**File:** `app/components/Welcome.tsx`

```tsx
export default function Welcome() {
  return (
    <section className="rounded-xl bg-white p-6 shadow-md">
      <h2 className="text-2xl font-bold text-gray-800">
        Server Component
      </h2>

      <p className="mt-2 text-gray-600">
        This component is rendered on the server by default.
      </p>
    </section>
  );
}
```

Use it in `app/page.tsx`:

```tsx
import Welcome from "./components/Welcome";

export default function Home() {
  return (
    <main className="p-6">
      <Welcome />
    </main>
  );
}
```

### Tailwind Classes

- `rounded-xl` → Rounded corners.
- `bg-white` → White background.
- `p-6` → Padding.
- `shadow-md` → Medium shadow.
- `text-2xl` → Large heading.

### We Learned

- App Router components are Server Components by default.
- Server Components can use Tailwind classes normally.
- They are useful for displaying content and fetching data on the server.
- A Server Component does not need `"use client"` just to apply styling.

</details>

---

<details>
<summary>04 — Client Component Styling</summary>

### Code

**File:** `app/components/Counter.tsx`

```tsx
"use client";

import { useState } from "react";

export default function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div className="rounded-xl border bg-white p-6 shadow-sm">
      <h2 className="text-xl font-bold">Client Component</h2>

      <p className="my-4 text-gray-600">
        Count: {count}
      </p>

      <button
        onClick={() => setCount(count + 1)}
        className="rounded-lg bg-indigo-600 px-4 py-2 text-white hover:bg-indigo-700"
      >
        Increase
      </button>
    </div>
  );
}
```

### Tailwind Classes

- `border` → Adds a border.
- `shadow-sm` → Small shadow.
- `my-4` → Vertical margin.
- `bg-indigo-600` → Indigo background.
- `hover:bg-indigo-700` → Darker background on hover.

### We Learned

- `"use client"` enables client-side interactivity.
- `useState` stores component state.
- `onClick` handles button clicks.
- Tailwind styling works in both Server and Client Components.

</details>

---

<details>
<summary>05 — Layout Styling</summary>

### Code

**File:** `app/dashboard/layout.tsx`

```tsx
export default function DashboardLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <div className="min-h-screen bg-gray-100">
      <header className="border-b bg-white px-6 py-4">
        <h1 className="text-xl font-bold text-indigo-600">
          My Dashboard
        </h1>
      </header>

      <div className="mx-auto max-w-7xl p-4 sm:p-6 lg:p-8">
        {children}
      </div>
    </div>
  );
}
```

### Tailwind Classes

- `border-b` → Bottom border.
- `px-6 py-4` → Horizontal and vertical padding.
- `mx-auto` → Centers the container.
- `max-w-7xl` → Limits maximum width.
- `sm:p-6` → More padding on small screens and above.
- `lg:p-8` → Larger padding on large screens and above.

### We Learned

- Layouts create a shared UI structure for a route section.
- The `children` prop displays the page inside the layout.
- Responsive padding improves the layout on different screen sizes.

</details>

---

<details>
<summary>06 — Page Styling</summary>

### Code

**File:** `app/dashboard/page.tsx`

```tsx
export default function DashboardPage() {
  return (
    <main className="space-y-6">
      <div>
        <h2 className="text-2xl font-bold sm:text-3xl">
          Dashboard Overview
        </h2>

        <p className="mt-2 text-sm text-gray-500">
          Welcome back! Here is your latest activity.
        </p>
      </div>

      <div className="grid grid-cols-1 gap-4 md:grid-cols-3">
        <div className="rounded-xl bg-white p-6 shadow-sm">
          <p className="text-sm text-gray-500">Total Revenue</p>
          <h3 className="mt-2 text-2xl font-bold">$12,500</h3>
        </div>

        <div className="rounded-xl bg-white p-6 shadow-sm">
          <p className="text-sm text-gray-500">Customers</p>
          <h3 className="mt-2 text-2xl font-bold">850</h3>
        </div>

        <div className="rounded-xl bg-white p-6 shadow-sm">
          <p className="text-sm text-gray-500">Orders</p>
          <h3 className="mt-2 text-2xl font-bold">320</h3>
        </div>
      </div>
    </main>
  );
}
```

### Tailwind Classes

- `space-y-6` → Vertical spacing between children.
- `text-2xl sm:text-3xl` → Responsive heading size.
- `grid-cols-1` → One column by default.
- `md:grid-cols-3` → Three columns on medium screens and above.
- `gap-4` → Space between grid items.

### We Learned

- A page file defines the content for its route.
- Dashboard cards can be organized with CSS Grid.
- Responsive utilities adapt the page to different screen sizes.

</details>

---

<details>
<summary>07 — Responsive Next.js Navbar</summary>

### Code

**File:** `app/components/Navbar.tsx`

```tsx
"use client";

import { useState } from "react";

export default function Navbar() {
  const [open, setOpen] = useState(false);

  return (
    <nav className="border-b bg-white px-4 py-4 sm:px-6">
      <div className="mx-auto flex max-w-7xl items-center justify-between">
        <a href="/" className="text-xl font-bold text-indigo-600">
          SaaSFlow
        </a>

        <button
          className="rounded border px-3 py-2 md:hidden"
          aria-expanded={open}
          aria-controls="mobile-menu"
          aria-label="Toggle navigation"
          onClick={() => setOpen(!open)}
        >
          ☰
        </button>

        <div className="hidden items-center gap-6 md:flex">
          <a href="/dashboard" className="text-gray-600 hover:text-indigo-600">
            Dashboard
          </a>
          <a href="/about" className="text-gray-600 hover:text-indigo-600">
            About
          </a>
          <a href="/login" className="text-gray-600 hover:text-indigo-600">
            Login
          </a>
        </div>
      </div>

      {open && (
        <div id="mobile-menu" className="mt-4 flex flex-col gap-3 md:hidden">
          <a href="/dashboard">Dashboard</a>
          <a href="/about">About</a>
          <a href="/login">Login</a>
        </div>
      )}
    </nav>
  );
}
```

### Tailwind Classes

- `flex` → Flexbox layout.
- `justify-between` → Places items at opposite ends.
- `hidden md:flex` → Hides links on small screens and displays them on medium screens and above.
- `md:hidden` → Hides the menu button on medium screens and above.
- `flex-col` → Stacks mobile links vertically.
- `gap-6` → Adds space between navigation links.

### We Learned

- How to create a responsive navbar.
- How to show a mobile menu with React state.
- How Tailwind breakpoints control navigation visibility.
- For internal production navigation, Next.js `Link` is generally preferred over a plain `<a>` element.

</details>

---

<details>
<summary>08 — Dashboard Layout</summary>

### Code

**File:** `app/components/Sidebar.tsx`

```tsx
import Link from "next/link";

export default function Sidebar() {
  return (
    <aside className="w-full border-b bg-white p-4 md:min-h-screen md:w-64 md:border-b-0 md:border-r">
      <h2 className="mb-6 text-lg font-bold">Workspace</h2>

      <nav className="flex flex-col gap-2">
        <Link
          href="/dashboard"
          className="rounded-lg bg-indigo-50 px-4 py-3 font-medium text-indigo-700"
        >
          Dashboard
        </Link>

        <Link
          href="/dashboard/projects"
          className="rounded-lg px-4 py-3 text-gray-600 hover:bg-gray-100"
        >
          Projects
        </Link>

        <Link
          href="/dashboard/settings"
          className="rounded-lg px-4 py-3 text-gray-600 hover:bg-gray-100"
        >
          Settings
        </Link>
      </nav>
    </aside>
  );
}
```

**File:** `app/dashboard/layout.tsx`

```tsx
import Sidebar from "../components/Sidebar";

export default function DashboardLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <div className="min-h-screen bg-gray-50 md:flex">
      <Sidebar />

      <main className="min-w-0 flex-1 p-4 sm:p-6 lg:p-8">
        {children}
      </main>
    </div>
  );
}
```

### Tailwind Classes

- `md:flex` → Creates a horizontal dashboard layout on medium screens and above.
- `md:w-64` → Gives the sidebar a fixed width.
- `md:border-r` → Adds a right border on desktop.
- `flex-1` → Allows the main content to use available space.
- `min-w-0` → Helps prevent flex content from overflowing.

### We Learned

- A dashboard usually has a sidebar and main content area.
- The sidebar can move above the content on small screens.
- A nested dashboard layout can be shared by dashboard pages.

</details>

---

<details>
<summary>09 — Authentication UI</summary>

### Code

**File:** `app/login/page.tsx`

```tsx
export default function LoginPage() {
  return (
    <main className="flex min-h-screen items-center justify-center bg-gray-100 p-4">
      <form className="w-full max-w-md space-y-5 rounded-2xl bg-white p-6 shadow-lg sm:p-8">
        <div className="text-center">
          <h1 className="text-3xl font-bold">Welcome Back</h1>
          <p className="mt-2 text-gray-500">
            Sign in to your account
          </p>
        </div>

        <div>
          <label htmlFor="email" className="mb-2 block text-sm font-medium">
            Email Address
          </label>
          <input
            id="email"
            name="email"
            type="email"
            autoComplete="email"
            required
            placeholder="you@example.com"
            className="w-full rounded-lg border border-gray-300 px-4 py-3 outline-none focus:border-indigo-500 focus:ring-2 focus:ring-indigo-100"
          />
        </div>

        <div>
          <label htmlFor="password" className="mb-2 block text-sm font-medium">
            Password
          </label>
          <input
            id="password"
            name="password"
            type="password"
            autoComplete="current-password"
            required
            placeholder="Enter your password"
            className="w-full rounded-lg border border-gray-300 px-4 py-3 outline-none focus:border-indigo-500 focus:ring-2 focus:ring-indigo-100"
          />
        </div>

        <button
          type="submit"
          className="w-full rounded-lg bg-indigo-600 py-3 font-semibold text-white hover:bg-indigo-700"
        >
          Sign In
        </button>
      </form>
    </main>
  );
}
```

### Tailwind Classes

- `items-center justify-center` → Centers the form.
- `max-w-md` → Limits the form width.
- `space-y-5` → Adds vertical spacing.
- `focus:border-indigo-500` → Changes border color when focused.
- `focus:ring-2` → Adds a focus ring.
- `w-full` → Makes the inputs and button full width.

### We Learned

- How to design a login form.
- How to style form labels and input fields.
- How to create visible focus states for keyboard and mouse users.

**Note:** This is only an authentication UI. A real login requires form submission, server-side credential verification, secure sessions, and appropriate authentication checks.

</details>

---

<details>
<summary>10 — Loading UI</summary>

### Code

**File:** `app/dashboard/loading.tsx`

```tsx
export default function Loading() {
  return (
    <div
      role="status"
      aria-label="Loading dashboard"
      className="space-y-6"
    >
      <div className="h-8 w-56 animate-pulse rounded bg-gray-200" />

      <div className="grid grid-cols-1 gap-4 md:grid-cols-3">
        <div className="h-32 animate-pulse rounded-xl bg-gray-200" />
        <div className="h-32 animate-pulse rounded-xl bg-gray-200" />
        <div className="h-32 animate-pulse rounded-xl bg-gray-200" />
      </div>

      <span className="sr-only">Loading...</span>
    </div>
  );
}
```

### Tailwind Classes

- `animate-pulse` → Creates a pulsing loading effect.
- `h-8` → Sets height.
- `w-56` → Sets width.
- `rounded` → Rounds the corners.
- `bg-gray-200` → Creates the placeholder background.
- `sr-only` → Makes text available to screen readers.

### We Learned

- Next.js App Router supports a special `loading.tsx` file.
- Loading skeletons show users that content is being prepared.
- Skeleton cards improve the perceived loading experience.

</details>

---

<details>
<summary>11 — Error UI</summary>

### Code

**File:** `app/dashboard/error.tsx`

```tsx
"use client";

export default function Error({
  reset,
}: {
  error: Error & { digest?: string };
  reset: () => void;
}) {
  return (
    <div className="flex min-h-[50vh] flex-col items-center justify-center p-6 text-center">
      <h2 className="text-2xl font-bold text-red-600">
        Something went wrong!
      </h2>

      <p className="mt-3 text-gray-600">
        We could not load this section. Please try again.
      </p>

      <button
        onClick={() => reset()}
        className="mt-6 rounded-lg bg-indigo-600 px-5 py-3 text-white hover:bg-indigo-700"
      >
        Try Again
      </button>
    </div>
  );
}
```

### Tailwind Classes

- `min-h-[50vh]` → Minimum height of half the viewport.
- `text-center` → Centers text.
- `text-red-600` → Red error heading.
- `mt-6` → Adds top margin.
- `hover:bg-indigo-700` → Changes button color on hover.

### We Learned

- `error.tsx` is a special App Router error boundary.
- It must be a Client Component.
- `reset()` attempts to render the failed segment again.
- Error screens should provide clear messages and recovery options.

</details>

---

<details>
<summary>12 — Not-Found UI</summary>

### Code

**File:** `app/not-found.tsx`

```tsx
import Link from "next/link";

export default function NotFound() {
  return (
    <main className="flex min-h-screen flex-col items-center justify-center bg-gray-50 p-6 text-center">
      <h1 className="text-7xl font-extrabold text-indigo-600">
        404
      </h1>

      <h2 className="mt-4 text-2xl font-bold">
        Page Not Found
      </h2>

      <p className="mt-3 max-w-md text-gray-600">
        Sorry, the page you are looking for does not exist.
      </p>

      <Link
        href="/"
        className="mt-6 rounded-lg bg-indigo-600 px-6 py-3 text-white hover:bg-indigo-700"
      >
        Back to Home
      </Link>
    </main>
  );
}
```

### Tailwind Classes

- `text-7xl` → Very large heading.
- `font-extrabold` → Extra-bold text.
- `max-w-md` → Limits paragraph width.
- `mt-4` → Adds top margin.
- `rounded-lg` → Rounded button-style link.

### We Learned

- `not-found.tsx` defines a custom not-found interface.
- `Link` lets users navigate back to the home page.
- A clear 404 page helps users recover from broken or missing routes.

</details>

---

<details>
<summary>13 — SEO-Friendly Responsive Layout</summary>

### Code

**File:** `app/layout.tsx`

```tsx
import type { Metadata } from "next";
import "./globals.css";

export const metadata: Metadata = {
  title: {
    default: "SaaSFlow Dashboard",
    template: "%s | SaaSFlow",
  },
  description:
    "Manage projects, customers, and business analytics with SaaSFlow.",
};

export default function RootLayout({
  children,
}: Readonly<{
  children: React.ReactNode;
}>) {
  return (
    <html lang="en">
      <body className="min-h-screen bg-gray-50 text-gray-900 antialiased">
        {children}
      </body>
    </html>
  );
}
```

**File:** `app/dashboard/page.tsx`

```tsx
import type { Metadata } from "next";

export const metadata: Metadata = {
  title: "Dashboard",
  description: "View your SaaSFlow business dashboard and statistics.",
};

export default function DashboardPage() {
  return (
    <main className="mx-auto w-full max-w-7xl p-4 sm:p-6 lg:p-8">
      <h1 className="text-2xl font-bold sm:text-3xl">
        Dashboard Overview
      </h1>

      <p className="mt-2 text-sm leading-6 text-gray-600 sm:text-base">
        Review your business performance on any device.
      </p>
    </main>
  );
}
```

### Tailwind Classes

- `antialiased` → Smooths font rendering.
- `mx-auto` → Centers the container.
- `w-full` → Uses available width.
- `max-w-7xl` → Limits content width.
- `sm:text-base` → Changes text size at the small breakpoint.
- `leading-6` → Sets line height.

### We Learned

- Next.js `metadata` defines page titles and descriptions.
- The root layout provides shared document structure.
- Responsive sizing and readable text improve the mobile experience.
- Good SEO also depends on useful page content, appropriate headings, accessible navigation, and crawlable pages.

</details>

---

<details>
<summary>14 — BUILD: Complete Next.js SaaS Dashboard</summary>

### Project Structure

Create these files inside your existing Next.js project:

```text
app/
├── components/
│   ├── Navbar.tsx
│   └── Sidebar.tsx
├── dashboard/
│   ├── layout.tsx
│   ├── loading.tsx
│   ├── error.tsx
│   └── page.tsx
├── login/
│   └── page.tsx
├── globals.css
├── layout.tsx
└── page.tsx
```

### Step 1 — Root Layout

**File:** `app/layout.tsx`

```tsx
import type { Metadata } from "next";
import "./globals.css";

export const metadata: Metadata = {
  title: "SaaSFlow | Business Dashboard",
  description:
    "A responsive SaaS dashboard built with Next.js and Tailwind CSS.",
};

export default function RootLayout({
  children,
}: Readonly<{
  children: React.ReactNode;
}>) {
  return (
    <html lang="en">
      <body className="min-h-screen bg-gray-50 text-gray-900 antialiased">
        {children}
      </body>
    </html>
  );
}
```

### Step 2 — Global CSS

**File:** `app/globals.css`

```css
@import "tailwindcss";

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}
```

If your project already has a working Tailwind v4 `globals.css`, keep its existing setup and add only the styles you need.

### Step 3 — Navbar

**File:** `app/components/Navbar.tsx`

```tsx
"use client";

import Link from "next/link";
import { useState } from "react";

export default function Navbar() {
  const [open, setOpen] = useState(false);

  return (
    <header className="border-b bg-white">
      <nav className="mx-auto flex max-w-7xl items-center justify-between px-4 py-4 sm:px-6">
        <Link
          href="/"
          className="text-2xl font-extrabold text-indigo-600"
        >
          SaaSFlow
        </Link>

        <button
          onClick={() => setOpen(!open)}
          aria-expanded={open}
          aria-controls="navbar-links"
          aria-label="Toggle navigation"
          className="rounded-lg border px-3 py-2 md:hidden"
        >
          ☰
        </button>

        <div
          id="navbar-links"
          className={`${open ? "flex" : "hidden"} absolute left-0 top-[65px] z-10 w-full flex-col gap-4 border-b bg-white p-5 md:static md:flex md:w-auto md:flex-row md:items-center md:border-0 md:p-0`}
        >
          <Link
            href="/dashboard"
            className="text-gray-600 hover:text-indigo-600"
          >
            Dashboard
          </Link>

          <Link
            href="/login"
            className="rounded-lg bg-indigo-600 px-4 py-2 text-center text-white hover:bg-indigo-700"
          >
            Sign In
          </Link>
        </div>
      </nav>
    </header>
  );
}
```

### Step 4 — Sidebar

**File:** `app/components/Sidebar.tsx`

```tsx
import Link from "next/link";

export default function Sidebar() {
  const links = [
    { label: "Overview", href: "/dashboard" },
    { label: "Projects", href: "/dashboard/projects" },
    { label: "Analytics", href: "/dashboard/analytics" },
    { label: "Settings", href: "/dashboard/settings" },
  ];

  return (
    <aside className="w-full shrink-0 border-b bg-white p-4 md:min-h-screen md:w-64 md:border-b-0 md:border-r">
      <h2 className="mb-5 px-3 text-xs font-bold uppercase tracking-wider text-gray-400">
        Workspace
      </h2>

      <nav className="flex flex-col gap-2">
        {links.map((link, index) => (
          <Link
            key={link.href}
            href={link.href}
            className={`rounded-lg px-4 py-3 text-sm font-medium ${
              index === 0
                ? "bg-indigo-50 text-indigo-700"
                : "text-gray-600 hover:bg-gray-100"
            }`}
          >
            {link.label}
          </Link>
        ))}
      </nav>
    </aside>
  );
}
```

### Step 5 — Dashboard Layout

**File:** `app/dashboard/layout.tsx`

```tsx
import Navbar from "../components/Navbar";
import Sidebar from "../components/Sidebar";

export default function DashboardLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <>
      <Navbar />

      <div className="mx-auto min-h-screen max-w-7xl md:flex">
        <Sidebar />

        <main className="min-w-0 flex-1 p-4 sm:p-6 lg:p-8">
          {children}
        </main>
      </div>
    </>
  );
}
```

### Step 6 — Dashboard Page

**File:** `app/dashboard/page.tsx`

```tsx
const stats = [
  {
    title: "Total Revenue",
    value: "$24,580",
    change: "+12.5%",
  },
  {
    title: "Total Customers",
    value: "1,240",
    change: "+8.2%",
  },
  {
    title: "Active Projects",
    value: "36",
    change: "+4.6%",
  },
  {
    title: "Conversion Rate",
    value: "6.8%",
    change: "+1.4%",
  },
];

const activities = [
  { name: "Website Redesign", status: "Completed" },
  { name: "Mobile App", status: "In Progress" },
  { name: "Marketing Campaign", status: "Pending" },
];

export default function DashboardPage() {
  return (
    <div className="space-y-8">
      <section className="flex flex-col justify-between gap-4 sm:flex-row sm:items-center">
        <div>
          <h1 className="text-2xl font-bold sm:text-3xl">
            Dashboard Overview
          </h1>
          <p className="mt-2 text-sm text-gray-500 sm:text-base">
            Welcome back! Here is your business summary.
          </p>
        </div>

        <button className="rounded-lg bg-indigo-600 px-5 py-3 font-medium text-white hover:bg-indigo-700">
          + New Project
        </button>
      </section>

      <section className="grid grid-cols-1 gap-5 sm:grid-cols-2 xl:grid-cols-4">
        {stats.map((stat) => (
          <article
            key={stat.title}
            className="rounded-2xl border border-gray-100 bg-white p-5 shadow-sm transition hover:shadow-md"
          >
            <p className="text-sm font-medium text-gray-500">
              {stat.title}
            </p>

            <h2 className="mt-3 text-2xl font-bold">
              {stat.value}
            </h2>

            <p className="mt-3 text-sm font-medium text-emerald-600">
              {stat.change} this month
            </p>
          </article>
        ))}
      </section>

      <section className="rounded-2xl border border-gray-100 bg-white p-5 shadow-sm sm:p-6">
        <div className="mb-5 flex items-center justify-between gap-3">
          <h2 className="text-lg font-bold">Recent Projects</h2>

          <span className="text-sm text-gray-500">
            3 projects
          </span>
        </div>

        <div className="overflow-x-auto">
          <table className="w-full min-w-[420px] text-left text-sm">
            <thead>
              <tr className="border-b text-gray-500">
                <th className="px-3 py-4 font-medium">Project</th>
                <th className="px-3 py-4 font-medium">Status</th>
              </tr>
            </thead>

            <tbody>
              {activities.map((activity) => (
                <tr
                  key={activity.name}
                  className="border-b last:border-0"
                >
                  <td className="px-3 py-4 font-medium">
                    {activity.name}
                  </td>

                  <td className="px-3 py-4">
                    <span
                      className={`inline-flex rounded-full px-3 py-1 text-xs font-semibold ${
                        activity.status === "Completed"
                          ? "bg-emerald-100 text-emerald-700"
                          : activity.status === "In Progress"
                            ? "bg-blue-100 text-blue-700"
                            : "bg-amber-100 text-amber-700"
                      }`}
                    >
                      {activity.status}
                    </span>
                  </td>
                </tr>
              ))}
            </tbody>
          </table>
        </div>
      </section>

      <footer className="border-t pt-5 text-center text-sm text-gray-500">
        © 2026 SaaSFlow. All rights reserved.
      </footer>
    </div>
  );
}
```

### Step 7 — Loading Screen

**File:** `app/dashboard/loading.tsx`

```tsx
export default function Loading() {
  return (
    <div role="status" aria-label="Loading dashboard" className="space-y-6">
      <div className="h-9 w-64 animate-pulse rounded bg-gray-200" />

      <div className="grid grid-cols-1 gap-5 sm:grid-cols-2 xl:grid-cols-4">
        {[1, 2, 3, 4].map((item) => (
          <div
            key={item}
            className="h-36 animate-pulse rounded-2xl bg-gray-200"
          />
        ))}
      </div>

      <div className="h-64 animate-pulse rounded-2xl bg-gray-200" />
      <span className="sr-only">Loading dashboard...</span>
    </div>
  );
}
```

### Step 8 — Error Screen

**File:** `app/dashboard/error.tsx`

```tsx
"use client";

export default function Error({
  reset,
}: {
  error: Error & { digest?: string };
  reset: () => void;
}) {
  return (
    <div className="flex min-h-[50vh] flex-col items-center justify-center text-center">
      <h2 className="text-2xl font-bold text-red-600">
        Unable to Load Dashboard
      </h2>

      <p className="mt-3 text-gray-500">
        Something went wrong. Please try again.
      </p>

      <button
        onClick={() => reset()}
        className="mt-5 rounded-lg bg-indigo-600 px-5 py-3 text-white hover:bg-indigo-700"
      >
        Try Again
      </button>
    </div>
  );
}
```

### Step 9 — Home Page

**File:** `app/page.tsx`

```tsx
import Link from "next/link";
import Navbar from "./components/Navbar";

export default function Home() {
  return (
    <>
      <Navbar />

      <main className="flex min-h-[80vh] items-center justify-center px-4 py-16">
        <section className="max-w-3xl text-center">
          <span className="rounded-full bg-indigo-100 px-4 py-2 text-sm font-semibold text-indigo-700">
            Your Business, Simplified
          </span>

          <h1 className="mt-6 text-4xl font-extrabold tracking-tight sm:text-5xl lg:text-6xl">
            Manage Your Business with{" "}
            <span className="text-indigo-600">SaaSFlow</span>
          </h1>

          <p className="mx-auto mt-6 max-w-2xl leading-7 text-gray-600">
            Track projects, review business statistics, and organize your
            workflow with a clean, responsive dashboard.
          </p>

          <Link
            href="/dashboard"
            className="mt-8 inline-flex rounded-lg bg-indigo-600 px-6 py-3 font-semibold text-white hover:bg-indigo-700"
          >
            Open Dashboard
          </Link>
        </section>
      </main>
    </>
  );
}
```

### Step 10 — Login UI

**File:** `app/login/page.tsx`

```tsx
export default function LoginPage() {
  return (
    <main className="flex min-h-screen items-center justify-center bg-gray-50 p-4">
      <form className="w-full max-w-md space-y-5 rounded-2xl border bg-white p-6 shadow-sm sm:p-8">
        <h1 className="text-center text-3xl font-bold">
          Sign In
        </h1>

        <div>
          <label htmlFor="email" className="mb-2 block text-sm font-medium">
            Email
          </label>

          <input
            id="email"
            name="email"
            type="email"
            required
            autoComplete="email"
            placeholder="you@example.com"
            className="w-full rounded-lg border px-4 py-3 outline-none focus:ring-2 focus:ring-indigo-200"
          />
        </div>

        <div>
          <label htmlFor="password" className="mb-2 block text-sm font-medium">
            Password
          </label>

          <input
            id="password"
            name="password"
            type="password"
            required
            autoComplete="current-password"
            placeholder="Enter password"
            className="w-full rounded-lg border px-4 py-3 outline-none focus:ring-2 focus:ring-indigo-200"
          />
        </div>

        <button
          type="submit"
          className="w-full rounded-lg bg-indigo-600 py-3 font-semibold text-white hover:bg-indigo-700"
        >
          Sign In
        </button>
      </form>
    </main>
  );
}
```

This login screen is a visual demo only. It does not authenticate a user or create a session.

### Step 11 — Run the Project

Open the terminal in VS Code and run:

```bash
npm run dev
```

Open these routes in your browser:

- `http://localhost:3000/` → Home page
- `http://localhost:3000/dashboard` → SaaS dashboard
- `http://localhost:3000/login` → Login UI

### Tailwind Classes

- `grid-cols-1 sm:grid-cols-2 xl:grid-cols-4` → Responsive dashboard cards.
- `rounded-2xl` → Rounded cards.
- `shadow-sm hover:shadow-md` → Shadow interaction.
- `overflow-x-auto` → Allows horizontal scrolling for the table on small screens.
- `transition` → Smoothly animates supported style changes.
- `text-emerald-600` → Green text for positive changes.
- `bg-amber-100` → Light amber status background.

### We Learned

- How to organize a Next.js App Router project.
- How to create reusable Navbar and Sidebar components.
- How to style pages and layouts with Tailwind CSS.
- How to build responsive statistic cards and a projects table.
- How to add login, loading, and error interfaces.
- How to define page metadata for SEO.
- How to use Next.js routes and nested layouts.

### Final Result

A responsive SaaS dashboard interface with:

* Responsive navigation
* Dashboard sidebar
* Business statistic cards
* Recent projects table
* Login screen UI
* Loading skeleton
* Error recovery screen
* SEO metadata

**Important:** This is a front-end dashboard demonstration with sample data. A production SaaS application still needs a database, authenticated sessions, authorization, real business data, and working form/API logic.

</details>

---

## Summary — UI.15

**What we learned:**

- Tailwind CSS styling in Next.js
- App Router pages and layouts
- Server and Client Components
- Responsive navigation and dashboard layouts
- Authentication, loading, error, and not-found UIs
- SEO metadata and responsive design
- Building a complete SaaS dashboard interface

**Next:** UI.16 — continue the next Tailwind CSS practice block in the same documentation format.
