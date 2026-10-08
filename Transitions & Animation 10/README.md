# Tailwind CSS Practice

## Transitions & Animation

Tailwind CSS provides utility classes for adding smooth transitions,
transforms, and animations to elements.

---

<details>
<summary>01 — Transition</summary>

### Code

```tsx
<div className="transition">
  Hover me
</div>
```
### Tailwind Class
transition
### ↓ We Learn
transition element ke changes ko smoothly show karta hai.
</details>

<details> <summary>02 — Transition Colors</summary>

### Code

```tsx
<button className="bg-blue-500 text-white transition-colors hover:bg-green-500">
  Hover Me
</button>
```
### Tailwind Class
transition-colors
### ↓ We Learn
transition-colors background aur text color changes ko smoothly animate karta hai.
</details>

<details> <summary>03 — Transition Transform</summary>

### Code

```tsx
<div className="transition-transform hover:scale-110">
  Hover Me
</div>
```
### Tailwind Class
transition-transform
### ↓ We Learn
transition-transform scale, rotate aur translate jaisi transform changes ko smooth banata hai.
</details>

<details> <summary>04 — Transition Opacity</summary>
  
### Code
```tsx
<div className="opacity-50 transition-opacity hover:opacity-100">
  Hover Me
</div>
```
### Tailwind Class
transition-opacity
### ↓ We Learn
transition-opacity element ki opacity change ko smoothly show karta hai.
</details>

<details> <summary>05 — Duration</summary>
  
### Code
```tsx
<button className="transition duration-1000 hover:scale-110">
  Hover Me
</button>
```
### Tailwind Class
duration-1000
### ↓ We Learn
duration transition ki speed/time control karta hai.
duration-1000 ka matlab transition 1000ms yani 1 second mein complete hoga.
</details>

<details> <summary>06 — Delay</summary>
  
### Code
```tsx
<button className="transition delay-300 hover:scale-110">
  Hover Me
</button>
```
### Tailwind Class
delay-300
### ↓ We Learn
delay transition start hone se pehle waiting time set karta hai.

</details>

<details> <summary>07 — Easing</summary>
  
### Code
```tsx
<button className="transition duration-500 ease-in-out hover:scale-110">
  Hover Me
</button>
```
### Tailwind Class
ease-in-out
### ↓ We Learn
ease-in-out transition ko start aur end par smoothly change karta hai.
</details>

<details> <summary>08 — Transform</summary>
  
### Code
```tsx
<div className="transition-transform hover:scale-110">
  Transform Me
</div>
```
### Tailwind Class
transition-transform
### ↓ We Learn
Transform ka use element ki position, size, rotation aur shape ko change karne ke liye hota hai.
</details>

<details> <summary>09 — Scale</summary>
  
### Code
```tsx
<div className="transition-transform hover:scale-125">
  Scale Me
</div>
```
### Tailwind Class
scale-125
### ↓ We Learn
scale element ka size increase ya decrease karta hai.
scale-125 element ko 125% size tak bada karta hai.
</details>

<details> <summary>10 — Rotate</summary>
  
### Code
```tsx
<div className="transition-transform hover:rotate-12">
  Rotate Me
</div>
```
### Tailwind Class
rotate-12
### ↓ We Learn
rotate element ko specific degree par rotate karta hai.
</details>

<details> <summary>11 — Translate</summary>
  
### Code
```tsx
<div className="transition-transform hover:translate-x-4">
  Move Me
</div>
```
### Tailwind Class
translate-x-4
### ↓ We Learn
translate element ko horizontal ya vertical direction mein move karta hai.
translate-x-4 element ko right side move karta hai.
</details>

<details> <summary>12 — Skew</summary>
  
### Code
```tsx
<div className="transition-transform hover:skew-x-6">
  Skew Me
</div>
```
### Tailwind Class
skew-x-6
### ↓ We Learn
skew element ko horizontally ya vertically slant karta hai.
</details>

<details> <summary>13 — Built-in Animations</summary>
  
### Code
```tsx
<div className="animate-spin">
  ⚙️
</div>
```
### Tailwind Class
animate-spin
### ↓ We Learn
Tailwind mein kuch built-in animations already available hoti hain.
</details>

<details> <summary>14 — animate-spin</summary>
  
### Code
```tsx
<div className="animate-spin">
  Loading...
</div>
```
### Tailwind Class
animate-spin
### ↓ We Learn
animate-spin element ko continuously rotate karta hai.
Ye loading icons ke liye useful hai.
</details>

<details> <summary>15 — animate-pulse</summary>
  
### Code
```tsx
<div className="animate-pulse bg-gray-300 p-6">
  Loading...
</div>
```
### Tailwind Class
animate-pulse
### ↓ We Learn
animate-pulse element ki opacity ko continuously change karta hai.
Ye loading skeletons ke liye useful hai.
</details>

<details> <summary>16 — animate-bounce</summary>
  
### Code
```tsx
<div className="animate-bounce">
  ↓
</div>
```
### Tailwind Class
animate-bounce
### ↓ We Learn
animate-bounce element ko continuously bounce karata hai.
</details>

<details> <summary>17 — Custom Animations</summary>
  
### Code
```tsx
@import "tailwindcss";

@theme {
  --animate-float: float 3s ease-in-out infinite;

  @keyframes float {
    0%, 100% {
      transform: translateY(0);
    }

    50% {
      transform: translateY(-10px);
    }
  }
}
<div className="animate-float">
  Floating Card
</div>
```
### Tailwind Class
animate-float
### ↓ We Learn
Custom animation ke liye hum apni @keyframes animation define kar sakte hain.
Phir us animation ko Tailwind class ke through use karte hain.
</details>

<details> <summary>18 — Build: Animated Product Cards</summary>
  
### Code
```tsx
<div className="grid grid-cols-1 gap-6 p-6 md:grid-cols-3">

  <div className="rounded-xl border p-5 shadow-md transition duration-300 hover:scale-105 hover:shadow-xl">

    <div className="mb-4 flex h-40 items-center justify-center rounded-lg bg-gray-100">
      Product Image
    </div>

    <h2 className="mb-2 text-xl font-bold">
      Product One
    </h2>

    <p className="mb-4 text-gray-600">
      Beautiful animated product card.
    </p>

    <button className="rounded-lg bg-blue-500 px-4 py-2 text-white transition-colors duration-300 hover:bg-blue-700">
      Buy Now
    </button>

  </div>


  <div className="rounded-xl border p-5 shadow-md transition duration-300 hover:scale-105 hover:shadow-xl">

    <div className="mb-4 flex h-40 items-center justify-center rounded-lg bg-gray-100">
      Product Image
    </div>

    <h2 className="mb-2 text-xl font-bold">
      Product Two
    </h2>

    <p className="mb-4 text-gray-600">
      Beautiful animated product card.
    </p>

    <button className="rounded-lg bg-blue-500 px-4 py-2 text-white transition-colors duration-300 hover:bg-blue-700">
      Buy Now
    </button>

  </div>


  <div className="rounded-xl border p-5 shadow-md transition duration-300 hover:scale-105 hover:shadow-xl">

    <div className="mb-4 flex h-40 items-center justify-center rounded-lg bg-gray-100">
      Product Image
    </div>

    <h2 className="mb-2 text-xl font-bold">
      Product Three
    </h2>

    <p className="mb-4 text-gray-600">
      Beautiful animated product card.
    </p>

    <button className="rounded-lg bg-blue-500 px-4 py-2 text-white transition-colors duration-300 hover:bg-blue-700">
      Buy Now
    </button>

  </div>

</div>
```
### Tailwind Classes

transition
duration-300
hover:scale-105
hover:shadow-xl
transition-colors
hover:bg-blue-700

### ↓ We Learn

Is project mein humne transitions aur animations ko practically use kiya.

Card hover karne par thora bara hota hai.
Card ki shadow smoothly change hoti hai.
Button ka background color smoothly change hota hai.
duration-300 animation ki speed control karta hai.
hover:scale-105 card ko hover par 105% tak bada karta hai.
Build

Animated product cards with hover scale, shadow and button transitions.

</details>



























