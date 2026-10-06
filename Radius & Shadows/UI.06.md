# Tailwind CSS Practice

## Borders, Radius & Shadows

Tailwind CSS provides utilities for borders, rounded corners, shadows, rings, and visual effects.

---

<details>
<summary>01 — Border Width</summary>

### Code
```tsx
<div className="border-4 border-blue-500 p-4">
  Border Width
</div>
```
### Tailwind Classes Used
* border-2 → 2px border
* border-4 → 4px border
* border-8 → 8px border
* border-blue-500 → Border color
### What We Learned
* Border width controls the thickness of an element's border.
* Tailwind provides different border width utilities.
</details>

<details> <summary>02 — Individual Borders</summary>

### Code
```tsx
<div className="border-t-4 border-b-2 border-blue-500 p-4">
  Individual Borders
</div>
```
### Tailwind Classes Used
* border-t-4 → Top border
* border-b-2 → Bottom border
* border-blue-500 → Border color
### What We Learned
* Individual borders can be applied to specific sides.
* border-t, border-b, border-l, and border-r control individual sides.
</details>

<details> <summary>03 — Border Styles</summary>

### Code
```tsx
<div className="border-4 border-dashed border-blue-500 p-4">
  Dashed Border
</div>
```
### Tailwind Classes Used
* border-solid
* border-dashed
* border-dotted
* border-double
### What We Learned
* Border styles control the appearance of the border.
* Tailwind provides solid, dashed, dotted, and double borders.
</details>

<details> <summary>04 — Border Radius</summary>

### Code
```tsx
<div className="border-2 border-blue-500  rounded-lg  p-4">
  Border Radius
</div>
```
### Tailwind Classes Used
* rounded
* rounded-md
* rounded-lg
* rounded-xl
* rounded-2xl
### What We Learned
* Border radius makes the corners of an element rounded.
* Larger rounded-* values create more rounded corners.
</details>

<details> <summary>05 — Rounded Cards</summary>

### Code
```tsx
<div className="w-80 rounded-xl bg-white p-6 shadow-md">
  <h2 className="text-2xl font-bold">
    Rounded Card
  </h2>
  <p className="mt-2 text-gray-600">
    This is a rounded card.
  </p>
</div>
```
### Tailwind Classes Used
* w-80 → Card width
* rounded-xl → Rounded corners
* bg-white → Background color
* p-6 → Padding
* shadow-md → Shadow
### What We Learned
* Rounded corners make cards look softer and more modern.
* rounded-xl is commonly used for cards.
</details>

<details> <summary>06 — Rounded Buttons</summary>
  
### Code
```tsx
<button className="rounded-full bg-blue-500 px-6 py-3 text-white">
  Get Started
</button>
```
### Tailwind Classes Used
* rounded-full → Fully rounded button
* bg-blue-500 → Button background
* px-6 → Horizontal padding
* py-3 → Vertical padding
* text-white → Text color
### What We Learned
* rounded-full creates a pill-shaped button.
* Rounded buttons are useful for modern UI designs.
</details>

<details> <summary>07 — Circular Elements</summary>
  
### Code
```tsx
<div className="flex h-24 w-24 items-center justify-center rounded-full bg-blue-500 text-white">
  A
</div>
```
### Tailwind Classes Used
* h-24 → Height
* w-24 → Width
* rounded-full → Circular shape
* flex → Flex container
* items-center → Vertical alignment
* justify-center → Horizontal alignment
### What We Learned
* Equal width and height with rounded-full creates a circle.
* Circular elements can be used for avatars, icons, and badges.
</details>

<details> <summary>08 — Shadows</summary>
  
### Code
```tsx
<div className="rounded-lg bg-white p-6 shadow-lg">
  Box Shadow
</div>
```
### Tailwind Classes Used
* shadow-sm
* shadow
* shadow-md
* shadow-lg
* shadow-xl
* shadow-2xl
### What We Learned
* Shadows add depth and elevation to elements.
* Different shadow sizes create different visual effects.
</details>

<details> <summary>09 — Custom Shadows</summary>
  
### Code
```tsx
<div className="rounded-xl bg-white p-6 shadow-[0_10px_30px_rgba(0,0,0,0.15)]">
  Custom Shadow
</div>
```
### Tailwind Classes Used
* shadow-[...] → Custom shadow value
* rounded-xl → Rounded corners
* p-6 → Padding
### What We Learned
* Tailwind allows custom shadow values using arbitrary values.
* Custom shadows give more control over the design.
</details>

<details> <summary>10 — Rings</summary>
  
### Code
```tsx
<div className="rounded-lg bg-white p-6 ring-4 ring-blue-500">
  Ring Effect
</div>
```
### Tailwind Classes Used
* ring-2
* ring-4
* ring-blue-500
* rounded-lg
### What We Learned
* Ring utilities create an outline around an element.
* Ring width and color can be customized.
</details>

<details> <summary>11 — Focus Rings</summary>
  
### Code
```tsx
<input
  className="rounded border border-gray-300 p-3 focus:ring-4 focus:ring-blue-300"
  placeholder="Enter your name"
/>
```
### Tailwind Classes Used
* border
* border-gray-300
* p-3
* focus:ring-4
* focus:ring-blue-300
### What We Learned
* focus: applies styles when an input receives focus.
* Focus rings help users identify the active input field.
</details>

<details> <summary>12 — Divide Utilities</summary>
  
### Code
```tsx
<div className="divide-y divide-gray-300">
  <div className="p-4">Item 1</div>
  <div className="p-4">Item 2</div>
  <div className="p-4">Item 3</div>
</div>
```
### Tailwind Classes Used
* divide-y → Adds dividers between vertical items
* divide-gray-300 → Divider color
* p-4 → Padding
### What We Learned
* Divide utilities add borders between child elements.
* divide-y is useful for lists and stacked content.
</details>

<details> <summary>13 — Border Opacity</summary>
  
### Code
```tsx
<div className="border-4 border-blue-500/50 p-6">
  Border Opacity
</div>
```
### Tailwind Classes Used
* border-4 → Border width
* border-blue-500/50 → 50% border opacity
* p-6 → Padding
### What We Learned
* Border opacity controls how transparent the border appears.
* Opacity can be added using / values such as /50.
</details>

<details> <summary>14 — Build: Modern Pricing Card</summary>
  
### Code
```tsx
<div className="mx-auto max-w-sm rounded-2xl border border-gray-200 bg-white p-6 shadow-md transition hover:-translate-y-1 hover:shadow-xl">

  <h2 className="text-2xl font-bold text-gray-900">
    Pro Plan
  </h2>

  <p className="mt-2 text-gray-500">
    Perfect for growing businesses.
  </p>

  <p className="mt-6 text-4xl font-bold">
    $29
    <span className="text-base font-normal text-gray-500">
      /month
    </span>
  </p>

  <button
    className="mt-6 w-full rounded-lg bg-blue-500 py-3 text-white
    transition hover:bg-blue-700
    focus:outline-none focus:ring-4 focus:ring-blue-300"
  >
    Get Started
  </button>

</div>
```
### Tailwind Classes Used
* max-w-sm → Limits card width
* rounded-2xl → Rounded card corners
* border → Adds border
* border-gray-200 → Border color
* shadow-md → Normal shadow
* hover:-translate-y-1 → Moves card slightly upward on hover
* hover:shadow-xl → Increases shadow on hover
* transition → Makes the effect smooth
* focus:ring-4 → Focus ring
* focus:ring-blue-300 → Focus ring color
### What We Learned
* How to combine borders, radius, and shadows.
* How to create hover elevation effects.
* How to add focus states to buttons.
* How to build a modern pricing card using Tailwind CSS.
</details> 









































