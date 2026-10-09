# Tailwind CSS Practice

## Advanced Tailwind

Advanced Tailwind CSS features allow us to create flexible, reusable, responsive, and accessible user interfaces using custom values, CSS variables, container queries, and advanced variants.

---

<details>
<summary>01 — Arbitrary Properties</summary>

### Code

```tsx
<div className="[mask-type:luminance]">
  Arbitrary Property Example
</div>
```

### Tailwind Class

`[mask-type:luminance]`

### ↓ We Learn

Arbitrary properties allow us to apply CSS properties that may not have a standard Tailwind utility class.

The CSS property and value are written inside square brackets.

</details>

---

<details>
<summary>02 — Arbitrary Values</summary>

### Code

```tsx
<div className="w-[350px] bg-[#2563eb] p-[25px] text-white">
  Custom Width and Color
</div>
```

### Tailwind Class

`w-[350px]` · `bg-[#2563eb]` · `p-[25px]`

### ↓ We Learn

Arbitrary values allow us to use custom CSS values instead of predefined Tailwind values.

For example, `w-[350px]` sets the width to exactly 350 pixels.

</details>

---

<details>
<summary>03 — Arbitrary Variants</summary>

### Code

```tsx
<ul className="[&>li]:border-b [&>li]:border-gray-300 [&>li]:p-3">
  <li>First Item</li>
  <li>Second Item</li>
  <li>Third Item</li>
</ul>
```

### Tailwind Class

`[&>li]:border-b` · `[&>li]:border-gray-300` · `[&>li]:p-3`

### ↓ We Learn

Arbitrary variants allow us to target specific child elements using custom CSS selectors.

Here, the styles are applied to every direct `li` child of the `ul`.

</details>

---

<details>
<summary>04 — Custom Utilities</summary>

### Code

Add a custom utility to `src/app/globals.css`:

```css
@import "tailwindcss";

@utility content-auto {
  content-visibility: auto;
}
```

Use it in a component:

```tsx
<div className="content-auto">
  This content uses a custom utility.
</div>
```

### Tailwind Class

`content-auto`

### ↓ We Learn

Custom utilities allow us to create reusable Tailwind classes for CSS properties that we use frequently.

The `@utility` directive registers a utility that can be used in HTML or JSX class names.

**Note:** If your CSS file already imports Tailwind, do not repeat the import. Add only the `@utility` definition.

</details>

---

<details>
<summary>05 — Custom Theme Values</summary>

### Code

Add this to `src/app/globals.css`:

```css
@import "tailwindcss";

@theme {
  --color-brand: #7c3aed;
  --font-display: "Arial", sans-serif;
  --breakpoint-3xl: 120rem;
}
```

Use the custom theme values:

```tsx
<div className="bg-brand font-display p-6 text-white">
  Custom Theme Example
</div>
```

### Tailwind Class

`bg-brand` · `font-display` · `3xl:`

### ↓ We Learn

Custom theme values allow us to define reusable colors, fonts, breakpoints, and other design tokens.

Tailwind can generate utilities from these theme variables.

</details>

---

<details>
<summary>06 — CSS Variables</summary>

### Code

```tsx
<div
  style={{ "--card-color": "#0f766e" } as React.CSSProperties}
  className="rounded-xl bg-[var(--card-color)] p-6 text-white"
>
  CSS Variable Example
</div>
```

### Tailwind Class

`bg-[var(--card-color)]`

### ↓ We Learn

CSS variables store reusable values such as colors, sizes, and spacing.

The `var(--card-color)` expression allows CSS to read the value stored in the variable.

</details>

---

<details>
<summary>07 — Container Queries</summary>

### Code

```tsx
<div className="@container max-w-2xl rounded-xl border p-4">
  <div className="flex flex-col gap-4 @md:flex-row">
    <div className="flex h-32 items-center justify-center rounded-lg bg-blue-100 p-4 @md:w-1/3">
      Image
    </div>

    <div className="@md:w-2/3">
      <h2 className="text-xl font-bold">Responsive Card</h2>
      <p className="mt-2 text-gray-600">
        This card changes its layout according to its container width.
      </p>
    </div>
  </div>
</div>
```

### Tailwind Class

`@container` · `@md:flex-row` · `@md:w-1/3`

### ↓ We Learn

Container queries allow an element to change its layout according to the size of its parent container rather than the entire screen.

</details>

---

<details>
<summary>08 — Advanced Responsive Layouts</summary>

### Code

```tsx
<div className="grid grid-cols-1 gap-4 sm:grid-cols-2 lg:grid-cols-3 2xl:grid-cols-4">
  <div className="rounded-lg bg-blue-100 p-6">Card 1</div>
  <div className="rounded-lg bg-green-100 p-6">Card 2</div>
  <div className="rounded-lg bg-purple-100 p-6">Card 3</div>
  <div className="rounded-lg bg-yellow-100 p-6">Card 4</div>
</div>
```

### Tailwind Class

`grid-cols-1` · `sm:grid-cols-2` · `lg:grid-cols-3` · `2xl:grid-cols-4`

### ↓ We Learn

Responsive utilities allow us to change layouts at different screen sizes.

* Mobile: one column
* Small screens: two columns
* Large screens: three columns
* Extra-large screens: four columns

</details>

---

<details>
<summary>09 — Complex Selectors</summary>

### Code

```tsx
<ul className="space-y-2 [&_li:first-child]:font-bold [&_li:nth-child(2)]:text-blue-600 [&_li:last-child]:text-green-600">
  <li>First Item</li>
  <li>Second Item</li>
  <li>Third Item</li>
</ul>
```

### Tailwind Class

`[&_li:first-child]:font-bold` · `[&_li:nth-child(2)]:text-blue-600` · `[&_li:last-child]:text-green-600`

### ↓ We Learn

Complex selectors allow us to target elements based on their position or relationship to other elements.

In this example, the first, second, and last list items receive different styles.

</details>

---

<details>
<summary>10 — Data Attributes</summary>

### Code

```tsx
<div
  data-status="active"
  className="rounded-lg border p-4 data-[status=active]:border-green-500 data-[status=active]:bg-green-50"
>
  Active Status
</div>

<div
  data-status="inactive"
  className="mt-3 rounded-lg border p-4 data-[status=inactive]:border-gray-400 data-[status=inactive]:bg-gray-100"
>
  Inactive Status
</div>
```

### Tailwind Class

`data-[status=active]:border-green-500` · `data-[status=inactive]:bg-gray-100`

### ↓ We Learn

Data attributes store custom information on HTML elements.

Tailwind's `data-*` variants allow us to apply styles according to an element's data attribute values.

</details>

---

<details>
<summary>11 — Accessibility Variants</summary>

### Code

```tsx
<button className="rounded-lg bg-blue-600 px-5 py-3 text-white hover:bg-blue-700 focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-blue-600">
  Accessible Button
</button>
```

### Tailwind Class

`focus-visible:outline-2` · `focus-visible:outline-offset-4` · `focus-visible:outline-blue-600`

### ↓ We Learn

Accessibility variants help us create interfaces that are easier to use with keyboards and assistive technologies.

The `focus-visible:` variant displays a visible focus indicator when appropriate, such as during keyboard navigation.

</details>

---

<details>
<summary>12 — Reduced-Motion Variants</summary>

### Code

```tsx
<button className="rounded-lg bg-purple-600 px-5 py-3 text-white transition-transform duration-300 hover:scale-110 motion-reduce:transform-none motion-reduce:transition-none">
  Hover Me
</button>
```

### Tailwind Class

`transition-transform` · `hover:scale-110` · `motion-reduce:transform-none` · `motion-reduce:transition-none`

### ↓ We Learn

The `motion-reduce:` variant allows us to reduce or remove animations for users who prefer reduced motion in their operating system settings.

</details>

---

<details>
<summary>13 — Print Styles</summary>

### Code

```tsx
<div className="rounded-xl bg-white p-6 shadow print:rounded-none print:bg-white print:p-0 print:shadow-none">
  <h2 className="text-2xl font-bold">Report</h2>

  <p className="mt-3 text-gray-700">
    This report can be printed without unnecessary shadows.
  </p>

  <button className="mt-4 rounded-lg bg-blue-600 px-4 py-2 text-white print:hidden">
    Print Report
  </button>
</div>
```

### Tailwind Class

`print:rounded-none` · `print:shadow-none` · `print:hidden`

### ↓ We Learn

Print variants allow us to apply different styles when a page is printed.

The `print:hidden` utility hides the button in the printed document.

</details>

---

<details>
<summary>14 — Build: Responsive Component Library</summary>

### Code

```tsx
export default function Home() {
  return (
    <main className="min-h-screen bg-gray-100 p-6 text-gray-900 sm:p-10">
      <header className="mx-auto mb-8 max-w-6xl">
        <h1 className="text-3xl font-bold tracking-tight sm:text-4xl">
          Component Library
        </h1>

        <p className="mt-2 text-gray-600">
          Reusable and responsive UI components built with Tailwind CSS.
        </p>
      </header>

      <section className="mx-auto grid max-w-6xl grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">

        <article className="@container rounded-xl border border-gray-200 bg-white p-5 shadow-sm transition-shadow hover:shadow-lg">
          <div className="flex flex-col gap-4 @md:flex-row">
            <div className="flex h-24 items-center justify-center rounded-lg bg-blue-100 text-2xl @md:w-24">
              UI
            </div>

            <div>
              <h2 className="text-xl font-bold">Card Component</h2>
              <p className="mt-2 text-gray-600">
                A reusable card with a container-responsive layout.
              </p>
            </div>
          </div>

          <button className="mt-5 w-full rounded-lg bg-blue-600 px-4 py-2 text-white transition-colors hover:bg-blue-700 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600">
            Learn More
          </button>
        </article>

        <article className="rounded-xl border border-gray-200 bg-white p-5 shadow-sm">
          <span className="inline-block rounded-full bg-green-100 px-3 py-1 text-sm font-medium text-green-800">
            Active
          </span>

          <h2 className="mt-4 text-xl font-bold">Status Component</h2>

          <p className="mt-2 text-gray-600">
            A status card using data attributes and custom styles.
          </p>

          <div
            data-status="active"
            className="mt-4 rounded-lg border p-3 data-[status=active]:border-green-500 data-[status=active]:bg-green-50"
          >
            System is running
          </div>
        </article>

        <article className="rounded-xl border border-gray-200 bg-white p-5 shadow-sm">
          <h2 className="text-xl font-bold">Accessibility</h2>

          <p className="mt-2 text-gray-600">
            A keyboard-friendly button with a visible focus indicator.
          </p>

          <button className="mt-4 rounded-lg bg-purple-600 px-4 py-2 text-white focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-purple-600 motion-reduce:transition-none">
            Accessible Action
          </button>
        </article>

      </section>

      <footer className="mx-auto mt-8 max-w-6xl rounded-xl bg-white p-5 print:hidden">
        <p className="text-sm text-gray-600">
          Responsive layouts · Reusable components · Accessibility
        </p>
      </footer>
    </main>
  );
}
```

### Tailwind Class

`@container` · `@md:flex-row` · `sm:grid-cols-2` · `lg:grid-cols-3` · `data-*` · `focus-visible:` · `motion-reduce:` · `print:hidden`

### ↓ We Learn

* Arbitrary values help us apply custom dimensions and colors.
* Custom utilities and theme values make our styles reusable.
* Container queries help components adapt to their parent width.
* Responsive utilities arrange components across screen sizes.
* Data attributes allow styles to respond to element states.
* Accessibility variants improve keyboard navigation.
* Reduced-motion variants respect users' motion preferences.
* Print variants help create cleaner printed documents.

### Build

**A responsive component library using advanced Tailwind features.**

</details>

**Important:**
This documentation uses Tailwind CSS v4 syntax. For the custom theme values, utilities, and dark-mode configuration, add the CSS definitions to your existing globals.css rather than duplicating the Tailwind import. The final Build component is intended for your Next.js page.tsx file, while the full document belongs in your GitHub Markdown file.
