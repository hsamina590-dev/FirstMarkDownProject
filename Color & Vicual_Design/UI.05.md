# Tailwind CSS Practice

## Colors & Visual Design

Tailwind CSS provides utility classes for colors, opacity, gradients, and visual styling.

---

<details>
<summary>01 — Tailwind Color System</summary>

**Code**

```tsx
<div className="bg-blue-500 text-white p-4">
  Tailwind Color System
</div>
```
### Tailwind Classes
* bg-blue-500
* text-white
* p-4

### What We Learned
* Tailwind provides a predefined color system.
* Colors can be applied to backgrounds and text.
</details>

<details> <summary>02 — Background Colors</summary>

**Code**

```tsx
<div className="bg-green-500 p-6">
  Background Color
</div>
```
### Tailwind Classes
* bg-green-500
* p-6

### What We Learned
 bg-* classes are used to change background colors.
</details>

<details> <summary>03 — Text Colors</summary>

**Code**

```tsx
<p className="text-red-500">
  Text Color
</p>
```
### Tailwind Classes
* text-red-500

### What We Learned
 text-* classes are used to change text colors.
</details>

<details> <summary>04 — Border Colors</summary>

**Code**

```tsx
<div className="border-2 border-blue-500 p-4">
  Border Color
</div>
```
### Tailwind Classes
* border-2
* border-blue-500
* p-4

### What We Learned
 border-* classes are used to style border colors.
</details>

<details> <summary>05 — Ring Colors</summary>

**Code**

```tsx
<input className="ring-2 ring-purple-500 p-2" placeholder="Enter text" />
```
### Tailwind Classes
* ring-2
* ring-purple-500
* p-2

### What We Learned
* Ring utilities add an outline-like ring around an element.
* Ring colors can be customized.
</details>

<details> <summary>06 — Opacity</summary>

```tsx
<div className="bg-blue-500/50 p-6 text-white">
  50% Opacity
</div>
```
### Tailwind Classes
* bg-blue-500/50
* p-6
* text-white

### What We Learned
* Opacity controls how transparent an element or color appears.
</details>

<details> <summary>07 — Color Combinations</summary>

```tsx
<div className="bg-blue-600 text-white border-2 border-blue-800 p-6">
  Color Combination
</div>
```
### Tailwind Classes
* bg-blue-600
* text-white
* border-2
* border-blue-800
* p-6

### What We Learned
* Different colors can be combined to create a clear visual design.
</details>

<details> <summary>08 — Neutral Color Palettes</summary>

```tsx
<div className="bg-gray-100 text-gray-800 p-6">
  Neutral Color Palette
</div>
```
### Tailwind Classes
* bg-gray-100
* text-gray-800
* p-6

### What We Learned
* Neutral colors such as gray are useful for backgrounds and readable text.
</details>

<details> <summary>09 — Brand Color Palettes</summary>

```tsx
<div className="bg-indigo-600 text-white p-6">
  Brand Color
</div>
```
### Tailwind Classes
* bg-indigo-600
* text-white
* p-6

### What We Learned
* Brand colors can be used consistently across a website.
</details>

<details> <summary>10 — Dark Color Palettes</summary>

```tsx
<div className="bg-gray-900 text-gray-100 p-6">
  Dark Color Palette
</div>
```
### Tailwind Classes
* bg-gray-900
* text-gray-100
* p-6

### What We Learned
* Dark colors can create a dark visual theme.
* Light text improves readability on dark backgrounds.
</details>

<details> <summary>11 — Gradient Backgrounds</summary>

```tsx
<div className="bg-gradient-to-r from-blue-500 to-purple-500 p-8 text-white">
  Gradient Background
</div>
```
### Tailwind Classes
* bg-gradient-to-r
* from-blue-500
* to-purple-500
* p-8
* text-white

### What We Learned
* Gradients combine two or more colors.
* from-* defines the starting color.
* to-* defines the ending color.
</details>

<details> <summary>12 — Gradient Text</summary>

```tsx
<h1 className="bg-gradient-to-r from-blue-500 to-purple-500 bg-clip-text text-transparent text-4xl font-bold">
  Gradient Text
</h1>
```
### Tailwind Classes
* bg-gradient-to-r
* from-blue-500
* to-purple-500
* bg-clip-text
* text-transparent
* text-4xl
* font-bold

### What We Learned
* Gradient colors can also be applied to text.
* bg-clip-text clips the gradient to the text.
</details>

<details> <summary>13 — Multi-Color Gradients</summary>

```tsx
<div className="bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 p-8 text-white">
  Multi-Color Gradient
</div>
```
### Tailwind Classes
* bg-gradient-to-r
* from-blue-500
* via-purple-500
* to-pink-500

### What We Learned
* via-* adds a middle color to a gradient.
* Multiple colors can create more complex visual effects.
</details>

<details> <summary>14 — Hover Color Changes</summary>

```tsx
<button className="bg-blue-500 hover:bg-blue-700 text-white px-6 py-3 rounded">
  Hover Me
</button>
```
### Tailwind Classes
* bg-blue-500
* hover:bg-blue-700
* text-white
* px-6
* py-3
* rounded
### What We Learned
* hover: changes a style when the user moves the mouse over an element.
* Hover effects make interactive elements more visually responsive.
</details>

<details> <summary>15 — Build a Modern SaaS Pricing Section</summary>

```tsx
<div className="max-w-5xl mx-auto p-6">

  <h1 className="text-4xl font-bold text-center mb-8">
    Choose Your Plan
  </h1>

  <div className="grid grid-cols-1 md:grid-cols-3 gap-6">

    <div className="border rounded-xl p-6 bg-white">
      <h2 className="text-2xl font-bold">Basic</h2>
      <p className="text-gray-500 mt-2">$9 / month</p>
      <button className="mt-6 w-full bg-blue-500 hover:bg-blue-700 text-white py-2 rounded">
        Get Started
      </button>
    </div>

    <div className="border-2 border-blue-500 rounded-xl p-6 bg-blue-50">
      <h2 className="text-2xl font-bold text-blue-600">Pro</h2>
      <p className="text-gray-600 mt-2">$29 / month</p>
      <button className="mt-6 w-full bg-blue-600 hover:bg-blue-800 text-white py-2 rounded">
        Choose Pro
      </button>
    </div>

    <div className="border rounded-xl p-6 bg-gray-900 text-white">
      <h2 className="text-2xl font-bold">Enterprise</h2>
      <p className="text-gray-300 mt-2">$59 / month</p>
      <button className="mt-6 w-full bg-white text-gray-900 py-2 rounded">
        Contact Us
      </button>
    </div>

  </div>
</div>
```
### Tailwind Classes
* bg-* → Background colors
* text-* → Text colors
* border-* → Border colors
* hover:* → Hover color changes
* bg-gradient-* → Gradient backgrounds
* grid → Pricing card layout
* md:grid-cols-3 → Responsive three-column layout
### What We Learned
* How to create a consistent color system.
* How to combine background, text, and border colors.
* How to use hover colors.
* How to create different visual themes.
* How to build a modern SaaS pricing section using Tailwind CSS.
</details>

















  
