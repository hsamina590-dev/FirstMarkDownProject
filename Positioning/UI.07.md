# Tailwind CSS Practice

## Positioning

Tailwind CSS positioning utilities help us control where elements appear on the page and how they interact with other elements.

---

<details>
<summary>01 — Relative</summary>

### Code

```tsx
<div className="relative h-32 w-64 bg-gray-200">
  Relative Element
</div>
```
### Tailwind Classes Used
relative → Sets the element position to relative.
h-32 → Sets height.
w-64 → Sets width.
### What We Learned
relative creates a positioning context for an element.
It is commonly used when positioning child elements absolutely.
</details>

<details> <summary>02 — Absolute</summary>
  
### Code
```tsx
<div className="relative h-32 w-64 bg-gray-200">
  <div className="absolute top-2 right-2 bg-blue-500 p-2 text-white">
    Absolute
  </div>
</div>
```
### Tailwind Classes Used
relative → Parent positioning context.
absolute → Positions the child absolutely.
top-2 → Moves the element from the top.
right-2 → Moves the element from the right.
### What We Learned
absolute positions an element relative to its nearest positioned parent.
</details>

<details> <summary>03 — Fixed</summary>
  
### Code
```tsx
<button className="fixed bottom-6 right-6 rounded-full bg-blue-500 p-4 text-white">
  +
</button>
```
### Tailwind Classes Used
fixed → Fixes the element relative to the viewport.
bottom-6 → Positions it from the bottom.
right-6 → Positions it from the right.
rounded-full → Makes it circular.
### What We Learned
fixed keeps an element in the same position while the page scrolls.
</details>

<details> <summary>04 — Sticky</summary>
  
### Code
```tsx
<nav className="sticky top-0 z-10 bg-white p-4 shadow">
  Sticky Navigation
</nav>
```
### Tailwind Classes Used
sticky → Makes the element sticky while scrolling.
top-0 → Sticks it to the top.
z-10 → Controls its layer.
shadow → Adds a shadow.
### What We Learned
sticky allows an element to stay visible while scrolling.
</details>

<details> <summary>05 — inset-*</summary>
  
### Code
```tsx
<div className="relative h-40 w-64 bg-gray-200">
  <div className="absolute inset-4 bg-blue-500 p-4 text-white">
    Inset
  </div>
</div>
```
### Tailwind Classes Used
relative
absolute
inset-4
### What We Learned
inset-* controls the top, right, bottom, and left position at the same time.
</details>

<details> <summary>06 — top-*</summary>
  
### Code
```tsx
<div className="relative h-32 bg-gray-200">
  <div className="absolute top-4 bg-blue-500 p-3 text-white">
    Top Position
  </div>
</div>
```
### Tailwind Classes Used
absolute
top-4
### What We Learned
top-* controls the distance from the top edge.
</details>

<details> <summary>07 — right-*</summary>
  
### Code
```tsx
<div className="relative h-32 bg-gray-200">
  <div className="absolute right-4 bg-blue-500 p-3 text-white">
    Right Position
  </div>
</div>
```
### Tailwind Classes Used
absolute
right-4
### What We Learned
right-* controls the distance from the right edge.
</details>

<details> <summary>08 — bottom-*</summary>
  
### Code
```tsx
<div className="relative h-32 bg-gray-200">
  <div className="absolute bottom-4 bg-blue-500 p-3 text-white">
    Bottom Position
  </div>
</div>
```
### Tailwind Classes Used
absolute
bottom-4
### What We Learned
bottom-* controls the distance from the bottom edge.
</details>

<details> <summary>09 — left-*</summary>
  
### Code
```tsx
<div className="relative h-32 bg-gray-200">
  <div className="absolute left-4 bg-blue-500 p-3 text-white">
    Left Position
  </div>
</div>
```
### Tailwind Classes Used
absolute
left-4
### What We Learned
left-* controls the distance from the left edge.
</details>

<details> <summary>10 — z-*</summary>
  
### Code
```tsx
<div className="relative h-32">
  <div className="absolute left-4 top-4 z-10 bg-blue-500 p-6 text-white">
    Front Layer
  </div>
  <div className="absolute left-10 top-8 z-0 bg-red-500 p-6 text-white">
    Back Layer
  </div>
</div>
```
### Tailwind Classes Used
relative
absolute
z-10
z-0
### What We Learned
z-* controls the stacking order of positioned elements.
A higher z-index places an element above elements with a lower z-index.
</details>

<details> <summary>11 — Layered Components</summary>
  
### Code
```tsx
<div className="relative h-40 w-64">
  <div className="absolute inset-0 rounded-xl bg-blue-500"></div>

  <div className="absolute left-6 top-6 rounded-xl bg-white p-6 shadow-lg">
    Layered Component
  </div>
</div>
```
### Tailwind Classes Used
relative
absolute
inset-0
left-6
top-6
shadow-lg
### What We Learned
Multiple positioned elements can be layered together.
Layering is useful for cards, overlays, and visual effects.
</details>

<details> <summary>12 — Absolute Badges</summary>
  
### Code
```tsx
<div className="relative w-64 rounded-xl bg-gray-100 p-6">
  Product Card

  <span className="absolute right-2 top-2 rounded-full bg-red-500 px-3 py-1 text-xs text-white">
    New
  </span>
</div>
```
### Tailwind Classes Used
relative
absolute
right-2
top-2
rounded-full
bg-red-500
### What We Learned
Absolute positioning is useful for placing badges inside cards.
The parent is usually set to relative.
</details>

<details> <summary>13 — Floating Buttons</summary>
  
### Code
```tsx
<button className="fixed bottom-6 right-6 rounded-full bg-blue-600 p-4 text-white shadow-lg hover:bg-blue-700">
  +
</button>
```
### Tailwind Classes Used
fixed
bottom-6
right-6
rounded-full
shadow-lg
hover:bg-blue-700
### What We Learned
Fixed positioning can create floating action buttons.
Floating buttons remain visible while scrolling.
</details>

<details> <summary>14 — Sticky Navigation</summary>
  
### Code
```tsx
<nav className="sticky top-0 z-50 bg-white p-4 shadow-md">
  <div className="flex justify-between">
    <span className="font-bold">My Website</span>

    <div className="flex gap-4">
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Contact</a>
    </div>
  </div>
</nav>
```
### Tailwind Classes Used
sticky
top-0
z-50
bg-white
shadow-md
flex
justify-between
### What We Learned
Sticky navigation remains visible during scrolling.
z-50 keeps the navigation above other content.
</details>

<details> <summary>15 — Modal Positioning</summary>
  
### Code
```tsx
<div className="fixed inset-0 flex items-center justify-center bg-black/50">
  <div className="w-96 rounded-xl bg-white p-6 shadow-2xl">
    <h2 className="text-2xl font-bold">
      Modal
    </h2>

    <p className="mt-2 text-gray-600">
      This is a modal window.
    </p>

    <button className="mt-6 rounded-lg bg-blue-500 px-5 py-2 text-white">
      Close
    </button>
  </div>
</div>
```
### Tailwind Classes Used
fixed
inset-0
flex
items-center
justify-center
bg-black/50
shadow-2xl
### What We Learned
fixed inset-0 can cover the complete viewport.
Flex utilities can center a modal.
A semi-transparent background creates an overlay.
</details>

<details> <summary>16 — Build: Dashboard with Sticky Navbar, Floating Notification Button and Modal</summary>
  
### Code
```tsx
<div className="min-h-screen bg-gray-100">

  {/* Sticky Navbar */}
  <nav className="sticky top-0 z-50 bg-white p-4 shadow-md">
    <div className="flex items-center justify-between">
      <h1 className="text-xl font-bold">
        Dashboard
      </h1>

      <div className="flex gap-4">
        <a href="#">Home</a>
        <a href="#">Profile</a>
        <a href="#">Settings</a>
      </div>
    </div>
  </nav>

  {/* Dashboard Content */}
  <main className="p-6">
    <div className="grid grid-cols-1 gap-6 md:grid-cols-3">

      <div className="rounded-xl bg-white p-6 shadow">
        <h2 className="font-bold">Users</h2>
        <p className="mt-2 text-3xl">120</p>
      </div>

      <div className="rounded-xl bg-white p-6 shadow">
        <h2 className="font-bold">Orders</h2>
        <p className="mt-2 text-3xl">85</p>
      </div>

      <div className="rounded-xl bg-white p-6 shadow">
        <h2 className="font-bold">Revenue</h2>
        <p className="mt-2 text-3xl">$5,240</p>
      </div>

    </div>
  </main>

  {/* Floating Notification Button */}
  <button className="fixed bottom-6 right-6 rounded-full bg-blue-600 p-4 text-white shadow-lg">
    🔔
  </button>

  {/* Modal */}
  <div className="fixed inset-0 flex items-center justify-center bg-black/50">
    <div className="w-96 rounded-xl bg-white p-6 shadow-2xl">
      <h2 className="text-2xl font-bold">
        Notification
      </h2>

      <p className="mt-2 text-gray-600">
        You have a new notification.
      </p>

      <button className="mt-6 rounded-lg bg-blue-500 px-5 py-2 text-white">
        Close
      </button>
    </div>
  </div>

</div>
```
### Tailwind Classes Used
sticky top-0 → Sticky navbar
fixed bottom-6 right-6 → Floating notification button
fixed inset-0 → Full-screen modal
z-50 → Controls the navbar layer
bg-black/50 → Modal overlay
flex items-center justify-center → Centers the modal
shadow-lg → Button shadow
shadow-2xl → Modal shadow
rounded-xl → Rounded cards and modal
### What We Learned
How to use relative and absolute positioning.
How to position elements from the top, right, bottom, and left.
How to use fixed and sticky positioning.
How to control layers with z-*.
How to create absolute badges.
How to create floating buttons.
How to create sticky navigation.
How to position a modal.
How to combine positioning utilities to build a complete dashboard.
</details> 

