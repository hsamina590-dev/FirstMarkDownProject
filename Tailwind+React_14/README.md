# Tailwind CSS Practice

## Tailwind + React

React allows us to build reusable UI components, while Tailwind CSS helps us style them using utility classes. Together, they make it easier to create consistent, maintainable, and responsive user interfaces.

---

<details>
<summary>01 — Conditional Classes</summary>

### Code

```tsx
"use client";

import { useState } from "react";

export default function ConditionalClasses() {
  const [isActive, setIsActive] = useState(false);

  return (
    <button
      onClick={() => setIsActive(!isActive)}
      className={`rounded-lg px-5 py-3 text-white ${
        isActive ? "bg-green-600" : "bg-gray-500"
      }`}
    >
      {isActive ? "Active" : "Inactive"}
    </button>
  );
}
```

### Tailwind Class

`bg-green-600` · `bg-gray-500` · `rounded-lg` · `px-5` · `py-3`

### ↓ We Learn

Conditional classes allow us to change styles based on a condition.

* When `isActive` is `true`, the button becomes green.
* When `isActive` is `false`, the button becomes gray.
* The `useState` hook stores the current state.

</details>

---

<details>
<summary>02 — Dynamic Classes</summary>

### Code

```tsx
"use client";

import { useState } from "react";

export default function DynamicClasses() {
  const [color, setColor] = useState("blue");

  const colorClasses: Record<string, string> = {
    blue: "bg-blue-600",
    green: "bg-green-600",
    purple: "bg-purple-600",
  };

  return (
    <div className="space-y-4">
      <div className={`rounded-lg p-6 text-white ${colorClasses[color]}`}>
        Selected Color: {color}
      </div>

      <div className="flex gap-3">
        <button onClick={() => setColor("blue")} className="rounded bg-blue-600 px-3 py-2 text-white">
          Blue
        </button>

        <button onClick={() => setColor("green")} className="rounded bg-green-600 px-3 py-2 text-white">
          Green
        </button>

        <button onClick={() => setColor("purple")} className="rounded bg-purple-600 px-3 py-2 text-white">
          Purple
        </button>
      </div>
    </div>
  );
}
```

### Tailwind Class

`bg-blue-600` · `bg-green-600` · `bg-purple-600` · `p-6`

### ↓ We Learn

Dynamic classes allow us to select styles at runtime based on application data or user actions.

We define complete Tailwind class names in `colorClasses` so Tailwind can detect and generate the required CSS.

</details>

---

<details>
<summary>03 — Reusable Components</summary>

### Code

```tsx
type ButtonProps = {
  label: string;
};

function CustomButton({ label }: ButtonProps) {
  return (
    <button className="rounded-lg bg-blue-600 px-5 py-2 text-white hover:bg-blue-700">
      {label}
    </button>
  );
}

export default function ReusableComponents() {
  return (
    <div className="flex flex-wrap gap-3">
      <CustomButton label="Login" />
      <CustomButton label="Register" />
      <CustomButton label="Explore" />
    </div>
  );
}
```

### Tailwind Class

`rounded-lg` · `bg-blue-600` · `px-5` · `py-2` · `hover:bg-blue-700`

### ↓ We Learn

Reusable components allow us to write a component once and use it multiple times.

Props such as `label` allow each instance to display different text without repeating the component's code.

</details>

---

<details>
<summary>04 — Card Component</summary>

### Code

```tsx
type CardProps = {
  title: string;
  description: string;
};

function Card({ title, description }: CardProps) {
  return (
    <div className="rounded-xl border border-gray-200 bg-white p-6 shadow-sm transition hover:shadow-lg">
      <h2 className="text-xl font-bold text-gray-900">
        {title}
      </h2>

      <p className="mt-2 text-gray-600">
        {description}
      </p>

      <button className="mt-4 rounded-lg bg-blue-600 px-4 py-2 text-white">
        Learn More
      </button>
    </div>
  );
}

export default function CardExample() {
  return (
    <div className="grid grid-cols-1 gap-4 md:grid-cols-2">
      <Card
        title="React"
        description="Build reusable user interfaces."
      />

      <Card
        title="Tailwind CSS"
        description="Style interfaces using utility classes."
      />
    </div>
  );
}
```

### Tailwind Class

`rounded-xl` · `border` · `p-6` · `shadow-sm` · `hover:shadow-lg`

### ↓ We Learn

A card component displays related content inside a reusable container.

Props allow us to reuse the same card design for products, services, profiles, and other content.

</details>

---

<details>
<summary>05 — Modal Component</summary>

### Code

```tsx
"use client";

import { useState } from "react";

export default function ModalExample() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <div>
      <button
        onClick={() => setIsOpen(true)}
        className="rounded-lg bg-blue-600 px-5 py-2 text-white"
      >
        Open Modal
      </button>

      {isOpen && (
        <div
          className="fixed inset-0 z-50 flex items-center justify-center bg-black/50 p-4"
          onClick={() => setIsOpen(false)}
        >
          <div
            role="dialog"
            aria-modal="true"
            aria-labelledby="modal-title"
            className="w-full max-w-md rounded-xl bg-white p-6 shadow-xl"
            onClick={(event) => event.stopPropagation()}
          >
            <h2 id="modal-title" className="text-xl font-bold">
              Welcome
            </h2>

            <p className="mt-3 text-gray-600">
              This is a reusable modal component.
            </p>

            <button
              onClick={() => setIsOpen(false)}
              className="mt-5 rounded-lg bg-red-600 px-4 py-2 text-white"
            >
              Close
            </button>
          </div>
        </div>
      )}
    </div>
  );
}
```

### Tailwind Class

`fixed` · `inset-0` · `z-50` · `bg-black/50` · `max-w-md`

### ↓ We Learn

A modal displays content in an overlay above the current page.

* `useState` controls whether the modal is open.
* `fixed inset-0` covers the viewport.
* Clicking the background closes the modal.
* `stopPropagation()` prevents clicks inside the modal from closing it.

This is a basic modal example. Production modals should also support Escape-key closing and focus management.

</details>

---

<details>
<summary>06 — Navbar Component</summary>

### Code

```tsx
function Navbar() {
  return (
    <nav className="flex flex-wrap items-center justify-between gap-4 bg-gray-900 px-6 py-4 text-white">
      <h1 className="text-2xl font-bold">
        MyWebsite
      </h1>

      <div className="flex gap-5">
        <a href="#home" className="hover:text-blue-400">
          Home
        </a>

        <a href="#about" className="hover:text-blue-400">
          About
        </a>

        <a href="#contact" className="hover:text-blue-400">
          Contact
        </a>
      </div>
    </nav>
  );
}

export default function NavbarExample() {
  return <Navbar />;
}
```

### Tailwind Class

`flex` · `flex-wrap` · `justify-between` · `bg-gray-900` · `hover:text-blue-400`

### ↓ We Learn

A navbar provides navigation links to different sections or pages.

Creating a reusable navbar helps maintain a consistent design across a website.

</details>

---

<details>
<summary>07 — Sidebar Component</summary>

### Code

```tsx
function Sidebar() {
  const links = ["Dashboard", "Profile", "Settings", "Logout"];

  return (
    <aside className="min-h-screen w-64 bg-gray-900 p-5 text-white">
      <h2 className="mb-6 text-xl font-bold">
        Admin Panel
      </h2>

      <nav className="space-y-2">
        {links.map((link) => (
          <a
            key={link}
            href="#"
            className="block rounded-lg px-4 py-3 hover:bg-gray-700"
          >
            {link}
          </a>
        ))}
      </nav>
    </aside>
  );
}

export default function SidebarExample() {
  return <Sidebar />;
}
```

### Tailwind Class

`min-h-screen` · `w-64` · `space-y-2` · `block` · `hover:bg-gray-700`

### ↓ We Learn

A sidebar displays navigation links vertically, often in dashboards and admin panels.

The `map()` method generates links from an array, avoiding repeated markup.

</details>

---

<details>
<summary>08 — Form Components</summary>

### Code

```tsx
type InputProps = {
  label: string;
  type?: string;
  placeholder: string;
};

function FormInput({
  label,
  type = "text",
  placeholder,
}: InputProps) {
  return (
    <label className="block">
      <span className="mb-1 block font-medium text-gray-700">
        {label}
      </span>

      <input
        type={type}
        placeholder={placeholder}
        className="w-full rounded-lg border border-gray-300 px-4 py-3 outline-none focus:border-blue-500 focus:ring-2 focus:ring-blue-200"
      />
    </label>
  );
}

export default function FormExample() {
  return (
    <form className="mx-auto max-w-md space-y-4">
      <FormInput label="Name" placeholder="Enter your name" />

      <FormInput
        label="Email"
        type="email"
        placeholder="Enter your email"
      />

      <FormInput
        label="Password"
        type="password"
        placeholder="Enter your password"
      />

      <button
        type="submit"
        className="w-full rounded-lg bg-blue-600 px-4 py-3 text-white hover:bg-blue-700"
      >
        Submit
      </button>
    </form>
  );
}
```

### Tailwind Class

`w-full` · `rounded-lg` · `border-gray-300` · `focus:ring-2` · `space-y-4`

### ↓ We Learn

Reusable form components help us maintain consistent labels, inputs, spacing, and focus styles across different forms.

**Note:** This example demonstrates styling. Actual form submission and validation require additional logic.

</details>

---

<details>
<summary>09 — Badge Component</summary>

### Code

```tsx
type BadgeProps = {
  label: string;
  color?: "green" | "red" | "blue";
};

function Badge({ label, color = "blue" }: BadgeProps) {
  const styles = {
    green: "bg-green-100 text-green-800",
    red: "bg-red-100 text-red-800",
    blue: "bg-blue-100 text-blue-800",
  };

  return (
    <span className={`inline-flex rounded-full px-3 py-1 text-sm font-medium ${styles[color]}`}>
      {label}
    </span>
  );
}

export default function BadgeExample() {
  return (
    <div className="flex flex-wrap gap-3">
      <Badge label="Active" color="green" />
      <Badge label="Error" color="red" />
      <Badge label="Information" color="blue" />
    </div>
  );
}
```

### Tailwind Class

`inline-flex` · `rounded-full` · `px-3` · `py-1` · `text-sm`

### ↓ We Learn

A badge displays a short label such as Active, Pending, Error, or New.

Props allow us to reuse the badge with different text and colors.

</details>

---

<details>
<summary>10 — Alert Component</summary>

### Code

```tsx
type AlertProps = {
  message: string;
  type?: "success" | "error" | "warning";
};

function Alert({ message, type = "success" }: AlertProps) {
  const styles = {
    success: "border-green-500 bg-green-50 text-green-800",
    error: "border-red-500 bg-red-50 text-red-800",
    warning: "border-yellow-500 bg-yellow-50 text-yellow-800",
  };

  return (
    <div
      role="alert"
      className={`rounded-lg border-l-4 p-4 ${styles[type]}`}
    >
      {message}
    </div>
  );
}

export default function AlertExample() {
  return (
    <div className="space-y-3">
      <Alert message="Your changes were saved successfully." type="success" />
      <Alert message="Something went wrong." type="error" />
      <Alert message="Please review your information." type="warning" />
    </div>
  );
}
```

### Tailwind Class

`border-l-4` · `rounded-lg` · `p-4` · `bg-green-50` · `bg-red-50`

### ↓ We Learn

An alert displays important messages to users.

We can create reusable success, error, and warning alerts by passing different props.

</details>

---

<details>
<summary>11 — Loading Component</summary>

### Code

```tsx
function Loading() {
  return (
    <div
      role="status"
      aria-live="polite"
      className="flex items-center gap-3 p-4"
    >
      <div className="h-6 w-6 animate-spin rounded-full border-4 border-gray-300 border-t-blue-600" />

      <span className="text-gray-600">
        Loading, please wait...
      </span>
    </div>
  );
}

export default function LoadingExample() {
  return <Loading />;
}
```

### Tailwind Class

`animate-spin` · `rounded-full` · `border-4` · `border-t-blue-600` · `flex`

### ↓ We Learn

A loading component informs users that content is being processed or fetched.

The `animate-spin` utility rotates the circular indicator continuously.

</details>

---

<details>
<summary>12 — Responsive Component Architecture</summary>

### Code

```tsx
type Product = {
  id: number;
  name: string;
  price: string;
};

function ProductCard({ name, price }: Omit<Product, "id">) {
  return (
    <article className="rounded-xl border bg-white p-5 shadow-sm">
      <div className="mb-4 flex h-32 items-center justify-center rounded-lg bg-gray-100">
        Product Image
      </div>

      <h2 className="text-lg font-bold">{name}</h2>

      <p className="mt-2 text-gray-600">{price}</p>

      <button className="mt-4 w-full rounded-lg bg-blue-600 px-4 py-2 text-white">
        View Product
      </button>
    </article>
  );
}

export default function ProductGrid() {
  const products: Product[] = [
    { id: 1, name: "Laptop", price: "$800" },
    { id: 2, name: "Headphones", price: "$100" },
    { id: 3, name: "Keyboard", price: "$50" },
  ];

  return (
    <section className="mx-auto grid max-w-6xl grid-cols-1 gap-5 sm:grid-cols-2 lg:grid-cols-3">
      {products.map((product) => (
        <ProductCard
          key={product.id}
          name={product.name}
          price={product.price}
        />
      ))}
    </section>
  );
}
```

### Tailwind Class

`grid-cols-1` · `sm:grid-cols-2` · `lg:grid-cols-3` · `gap-5` · `max-w-6xl`

### ↓ We Learn

Responsive component architecture means organizing an interface into reusable components that adapt to different screen sizes.

* `ProductCard` defines one reusable card.
* `products.map()` renders cards from data.
* `key` uniquely identifies each item.
* Responsive grid classes adjust the number of columns based on screen width.

</details>

---

<details>
<summary>13 — Build: Reusable React UI Component Library</summary>

### Code

Create this example in your Next.js `app/page.tsx` or `src/app/page.tsx` file. It combines reusable buttons, cards, badges, alerts, and a responsive navbar into one small UI library.

```tsx
type ButtonProps = {
  children: React.ReactNode;
  variant?: "primary" | "secondary";
};

function Button({ children, variant = "primary" }: ButtonProps) {
  const styles = {
    primary: "bg-blue-600 text-white hover:bg-blue-700",
    secondary: "bg-gray-200 text-gray-900 hover:bg-gray-300",
  };

  return (
    <button
      className={`rounded-lg px-4 py-2 font-medium transition-colors ${styles[variant]}`}
    >
      {children}
    </button>
  );
}

function Badge({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <span className="rounded-full bg-green-100 px-3 py-1 text-sm font-medium text-green-800">
      {children}
    </span>
  );
}

function Card({
  title,
  description,
}: {
  title: string;
  description: string;
}) {
  return (
    <article className="rounded-xl border border-gray-200 bg-white p-5 shadow-sm transition hover:shadow-lg">
      <div className="mb-4 flex items-center justify-between gap-3">
        <h2 className="text-xl font-bold">{title}</h2>
        <Badge>Active</Badge>
      </div>

      <p className="mb-5 text-gray-600">{description}</p>

      <div className="flex flex-wrap gap-3">
        <Button>Explore</Button>
        <Button variant="secondary">Details</Button>
      </div>
    </article>
  );
}

function Navbar() {
  return (
    <nav className="flex flex-wrap items-center justify-between gap-4 bg-gray-900 px-6 py-4 text-white">
      <h1 className="text-xl font-bold">UI Library</h1>

      <div className="flex gap-4 text-sm">
        <a href="#components" className="hover:text-blue-300">
          Components
        </a>
        <a href="#about" className="hover:text-blue-300">
          About
        </a>
      </div>
    </nav>
  );
}

export default function Home() {
  return (
    <main className="min-h-screen bg-gray-50">
      <Navbar />

      <section id="about" className="mx-auto max-w-6xl px-6 py-10">
        <h1 className="text-3xl font-bold tracking-tight sm:text-4xl">
          Reusable React Components
        </h1>

        <p className="mt-3 max-w-2xl text-gray-600">
          A collection of reusable, responsive, and consistent UI components
          built with React and Tailwind CSS.
        </p>

        <div
          id="components"
          className="mt-8 grid grid-cols-1 gap-5 sm:grid-cols-2 lg:grid-cols-3"
        >
          <Card
            title="Card Component"
            description="Reusable cards with titles, descriptions, badges, and action buttons."
          />

          <Card
            title="Button Component"
            description="Consistent buttons with primary and secondary styles."
          />

          <Card
            title="Responsive Layout"
            description="A flexible grid that adapts to mobile, tablet, and desktop screens."
          />
        </div>

        <div className="mt-8 rounded-xl border border-green-200 bg-green-50 p-5 text-green-900">
          <h2 className="font-bold">Success</h2>
          <p className="mt-1">
            Your reusable component library is ready to explore.
          </p>
        </div>
      </section>
    </main>
  );
}
```

### Tailwind Class

`rounded-xl` · `bg-blue-600` · `hover:bg-blue-700` · `transition-colors` · `grid-cols-1` · `sm:grid-cols-2` · `lg:grid-cols-3` · `max-w-6xl`

### ↓ We Learn

* React components let us divide a UI into reusable parts.
* Props allow components to display different content.
* Conditional and dynamic classes allow styles to change based on values.
* Tailwind utilities provide consistent spacing, colors, borders, and layouts.
* Responsive grid classes adapt the component library to different screens.
* Reusing components reduces duplication and makes projects easier to maintain.

### Build

**A reusable React UI component library using Tailwind CSS.**

</details>

### Important notes for VS Code

* The individual examples in sections 01–12 are separate learning examples. Run each in its own page/component when practising; don't paste all the export default examples into one file.

* The final Build section is a complete standalone page.tsx example. It does not need "use client" because it doesn't use hooks or browser event handlers.

* The modal and other interactive examples that use useState need "use client"; at the top of their own file in Next.js.

* The complete document belongs in ui.14.md on GitHub; the TSX examples belong in your actual React/Next.js files when you practise them
