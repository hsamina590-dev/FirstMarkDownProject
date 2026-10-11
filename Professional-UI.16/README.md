# UI.16 — NexaFlow

## Simple Website Using Tailwind CSS

NexaFlow is a simple, modern, and responsive website created using Next.js, React, TypeScript, and Tailwind CSS.

<details>
<summary>01 — Navbar</summary>

### Code

```tsx
<nav className="flex items-center justify-between bg-slate-900 p-4 text-white">
  <h1 className="text-2xl font-bold">NexaFlow</h1>
  <div className="flex gap-4">
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </div>
</nav>
```

### Tailwind Classes

* `flex` → Creates a flexible layout.
* `items-center` → Aligns items vertically.
* `justify-between` → Places items at opposite ends.
* `bg-slate-900` → Adds a dark background.
* `p-4` → Adds padding.
* `text-white` → Changes text color.
* `font-bold` → Makes text bold.
* `gap-4` → Adds space between links.

### We Learned

We learned how to create a simple navigation bar using Tailwind CSS.

</details>

<details>
<summary>02 — Hero Section</summary>

### Code

```tsx
<section
  id="home"
  className="bg-blue-50 px-6 py-20 text-center"
>
  <h2 className="text-4xl font-bold text-slate-900">
    Build Something Amazing
  </h2>

  <p className="mx-auto mt-4 max-w-xl text-lg text-slate-600">
    Create modern digital experiences with NexaFlow.
  </p>

  <a
    href="#contact"
    className="mt-6 inline-block rounded-lg bg-blue-600 px-6 py-3 text-white hover:bg-blue-700"
  >
    Get Started
  </a>
</section>
```

### Tailwind Classes

* `bg-blue-50` → Adds a light blue background.
* `px-6` → Adds horizontal padding.
* `py-20` → Adds vertical padding.
* `text-center` → Centers the text.
* `text-4xl` → Sets a large font size.
* `max-w-xl` → Limits the paragraph width.
* `mx-auto` → Centers the paragraph.
* `mt-4` → Adds top margin.
* `rounded-lg` → Rounds the corners.
* `hover:bg-blue-700` → Changes the button background on hover.

### We Learned

We learned how to create a hero section with a heading, description, and call-to-action button.

</details>

<details>
<summary>03 — About Section</summary>

### Code

```tsx
<section id="about" className="px-6 py-16">
  <h2 className="text-center text-3xl font-bold">
    About NexaFlow
  </h2>

  <p className="mx-auto mt-4 max-w-2xl text-center leading-7 text-slate-600">
    NexaFlow helps people explore simple and modern digital
    solutions with a clean and user-friendly design.
  </p>
</section>
```

### Tailwind Classes

* `py-16` → Adds vertical spacing.
* `text-3xl` → Sets the heading size.
* `text-center` → Centers the content.
* `max-w-2xl` → Controls the maximum width.
* `leading-7` → Increases line spacing.
* `text-slate-600` → Applies a gray text color.

### We Learned

We learned how to organize content in an About section.

</details>

<details>
<summary>04 — Feature Cards</summary>

### Code

```tsx
<section className="bg-slate-50 px-6 py-16">
  <h2 className="mb-10 text-center text-3xl font-bold">
    Our Features
  </h2>

  <div className="mx-auto grid max-w-5xl grid-cols-1 gap-6 md:grid-cols-3">
    <div className="rounded-xl bg-white p-6 shadow">
      <h3 className="text-xl font-semibold">Simple Design</h3>
      <p className="mt-3 text-slate-600">
        Clean layouts that are easy to understand.
      </p>
    </div>

    <div className="rounded-xl bg-white p-6 shadow">
      <h3 className="text-xl font-semibold">Responsive</h3>
      <p className="mt-3 text-slate-600">
        Layouts that adapt to different screen sizes.
      </p>
    </div>

    <div className="rounded-xl bg-white p-6 shadow">
      <h3 className="text-xl font-semibold">Modern UI</h3>
      <p className="mt-3 text-slate-600">
        A modern interface with consistent styling.
      </p>
    </div>
  </div>
</section>
```

### Tailwind Classes

* `grid` → Creates a grid layout.
* `grid-cols-1` → Displays one column by default.
* `md:grid-cols-3` → Displays three columns on medium screens and larger.
* `gap-6` → Adds space between cards.
* `rounded-xl` → Creates rounded corners.
* `bg-white` → Sets a white background.
* `shadow` → Adds a shadow.
* `font-semibold` → Applies semi-bold text.

### We Learned

We learned how to build reusable-looking feature cards with a responsive grid.

</details>

<details>
<summary>05 — Contact Section</summary>

### Code

```tsx
<section id="contact" className="px-6 py-16">
  <div className="mx-auto max-w-xl text-center">
    <h2 className="text-3xl font-bold">Contact Us</h2>

    <p className="mt-4 text-slate-600">
      Have a question? We would love to hear from you.
    </p>

    <a
      href="mailto:hello@nexaflow.example"
      className="mt-6 inline-block rounded-lg bg-slate-900 px-6 py-3 text-white hover:bg-slate-700"
    >
      Email Us
    </a>
  </div>
</section>
```

### Tailwind Classes

* `max-w-xl` → Limits the content width.
* `text-center` → Centers the content.
* `inline-block` → Allows the link to use padding and margin.
* `mailto:` → Opens the user's default email application.
* `hover:bg-slate-700` → Changes the background on hover.

### We Learned

We learned how to create a simple contact section with an email link.

</details>

<details>
<summary>06 — Footer</summary>

### Code

```tsx
<footer className="bg-slate-900 px-6 py-6 text-center text-white">
  <p>© 2026 NexaFlow. All rights reserved.</p>
</footer>
```

### Tailwind Classes

* `bg-slate-900` → Adds a dark background.
* `px-6` → Adds horizontal padding.
* `py-6` → Adds vertical padding.
* `text-center` → Centers the text.
* `text-white` → Makes the text white.

### We Learned

We learned how to create a simple footer for a website.

</details>

<details>
<summary>07 — Build: Simple NexaFlow Website</summary>

### Project Goal

Build a simple website that includes:

* Navbar
* Hero section
* About section
* Feature cards
* Contact section
* Footer

### What We Learned

* How to structure a simple website.
* How to use Tailwind CSS utility classes.
* How to create layouts using Flexbox and Grid.
* How to style buttons, cards, headings, and paragraphs.
* How to create a responsive layout.

</details>
