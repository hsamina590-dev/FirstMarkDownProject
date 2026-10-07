# Tailwind CSS Practice

## Images & Backgrounds

Tailwind CSS provides utilities for background images, gradients, overlays, object positioning, image sizing, and responsive image layouts.

---

<details>
<summary>01 — Background Images</summary>

### Code

```tsx
<div
  className="h-64 bg-cover bg-center"
  style={{
    backgroundImage:
      "url('https://images.unsplash.com/photo-1518770660439-4636190af475')",
  }}
>
  <h2 className="p-6 text-3xl font-bold text-white">
    Background Image
  </h2>
</div>
```

### Tailwind Classes Used
h-64 → Sets the height.
bg-cover → Makes the background cover the container.
bg-center → Centers the background image.
text-white → Makes text white.
### What We Learned
How to add a background image to an element.
How to control the background image size and position.
</details>

<details> <summary>02 — Background Positioning</summary>
  
### Code

```tsx
<div
  className="h-64 bg-cover bg-top"
  style={{
    backgroundImage:
      "url('https://images.unsplash.com/photo-1516321318423-f06f85e504b3')",
  }}
>
  <h2 className="p-6 text-2xl font-bold text-white">
    Background Position
  </h2>
</div>
```
### Tailwind Classes Used
bg-top → Positions the image at the top.
bg-center → Positions the image at the center.
bg-bottom → Positions the image at the bottom.
bg-left → Positions the image to the left.
bg-right → Positions the image to the right.

### What We Learned
Background positioning controls which part of an image is visible.
Tailwind provides different background position utilities.
</details>

<details> <summary>03 — Background Sizing</summary>
  
### code
```tsx
<div
  className="h-64 bg-no-repeat bg-contain bg-center"
  style={{
    backgroundImage:
      "url('https://images.unsplash.com/photo-1517245386807-bb43f82c33c4')",
  }}
>
  <h2 className="p-6 text-2xl font-bold">
    Background Sizing
  </h2>
</div>
```
### Tailwind Classes Used
bg-contain → Fits the complete image inside the container.
bg-cover → Covers the complete container.
bg-no-repeat → Prevents the image from repeating.
bg-center → Centers the image.

### What We Learned
Background sizing controls how an image fits inside its container.
bg-cover and bg-contain are commonly used for background images.
</details>

<details> <summary>04 — bg-cover</summary>
  
### code
```tsx
<div
  className="h-64 bg-cover bg-center"
  style={{
    backgroundImage:
      "url('https://images.unsplash.com/photo-1485827404703-89b55fcc595e')",
  }}
>
  <h2 className="p-6 text-3xl font-bold text-white">
    Background Cover
  </h2>
</div>
```
### Tailwind Classes Used
bg-cover
bg-center
h-64

### What We Learned
bg-cover makes the background image cover the entire container.
Some parts of the image may be cropped.
</details>

<details> <summary>05 — bg-contain</summary>
  
### code
```tsx
<div
  className="h-64 bg-contain bg-center bg-no-repeat bg-gray-100"
  style={{
    backgroundImage:
      "url('https://images.unsplash.com/photo-1488590528505-98d2b5aba04b')",
  }}
>
  <h2 className="p-6 text-2xl font-bold">
    Background Contain
  </h2>
</div>
```
### Tailwind Classes Used
bg-contain
bg-center
bg-no-repeat
bg-gray-100
### What We Learned
bg-contain keeps the complete background image visible.
Empty space may remain around the image.
</details>

<details> <summary>06 — Background Gradients</summary>
  
### code
```tsx
<div className="h-64 bg-gradient-to-r from-blue-500 to-purple-600 p-8">
  <h2 className="text-3xl font-bold text-white">
    Background Gradient
  </h2>
</div>
```
### Tailwind Classes Used
bg-gradient-to-r → Gradient from left to right.
from-blue-500 → Starting color.
to-purple-600 → Ending color.
text-white → White text.

### What We Learned
Gradients create smooth transitions between colors.
Tailwind provides different gradient directions and colors.
</details>

<details> <summary>07 — Background Overlays</summary>

### code
```tsx
<div
  className="relative h-64 bg-cover bg-center"
  style={{
    backgroundImage:
      "url('https://images.unsplash.com/photo-1519389950473-47ba0277781c')",
  }}
>
  <div className="absolute inset-0 bg-black/50"></div>

  <div className="relative z-10 p-8 text-white">
    <h2 className="text-3xl font-bold">
      Background Overlay
    </h2>
  </div>
</div>
```
### Tailwind Classes Used
relative → Creates a positioning context.
absolute → Positions the overlay.
inset-0 → Covers the complete container.
bg-black/50 → Creates a semi-transparent black overlay.
relative z-10 → Places the text above the overlay.

### What We Learned
Overlays improve text readability over background images.
bg-black/50 creates a 50% transparent black layer.
</details>

<details> <summary>08 — Object Positioning</summary>

### code
```tsx
<img
  src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3"
  className="h-64 w-full object-cover object-top"
  alt="Workspace"
/>
```
### Tailwind Classes Used
object-cover → Covers the image container.
object-top → Positions the image toward the top.
h-64 → Sets height.
w-full → Sets full width.

### What We Learned
Object positioning controls which part of an image is displayed.
object-top, object-center, and object-bottom change the visible position.
</details>

<details> <summary>09 — Object Fit</summary>

### code
```tsx
<img
  src="https://images.unsplash.com/photo-1498050108023-c5249f4df085"
  className="h-64 w-full object-contain bg-gray-100"
  alt="Laptop"
/>
```
### Tailwind Classes Used
object-contain → Keeps the complete image visible.
object-cover → Covers the complete container.
w-full → Full width.
h-64 → Sets height.

### What We Learned
Object fit controls how an image fits inside its container.
object-cover may crop the image.
object-contain keeps the whole image visible.
</details>

<details> <summary>10 — Image Aspect Ratios</summary>

### code
```tsx
<div className="aspect-video overflow-hidden rounded-xl">
  <img
    src="https://images.unsplash.com/photo-1497366754035-f200968a6e72"
    className="h-full w-full object-cover"
    alt="Office"
  />
</div>
```
### Tailwind Classes Used
aspect-video → Creates a 16:9 aspect ratio.
overflow-hidden → Hides overflowing image parts.
rounded-xl → Rounds the corners.
object-cover → Covers the image area.

### What We Learned
Aspect ratio keeps an image container proportional.
aspect-video is useful for videos, banners, and images.
</details>

<details> <summary>11 — Image Cards</summary>

### code
```tsx
<div className="max-w-sm overflow-hidden rounded-xl bg-white shadow-lg">

  <img
    src="https://images.unsplash.com/photo-1497366811353-6870744d04b2"
    className="h-48 w-full object-cover"
    alt="Modern Office"
  />

  <div className="p-6">
    <h2 className="text-2xl font-bold">
      Modern Workspace
    </h2>

    <p className="mt-2 text-gray-600">
      A simple image card using Tailwind CSS.
    </p>
  </div>

</div>
```
### Tailwind Classes Used
max-w-sm → Limits card width.
overflow-hidden → Keeps the image inside rounded corners.
rounded-xl → Rounded corners.
shadow-lg → Adds shadow.
object-cover → Fits image into the card.
p-6 → Adds padding.

### What We Learned
How to combine images with card layouts.
How to create clean image cards using Tailwind utilities.
</details>

<details> <summary>12 — Hero Image Overlays</summary>
  
### code
```tsx
<section
  className="relative h-96 bg-cover bg-center"
  style={{
    backgroundImage:
      "url('https://images.unsplash.com/photo-1518770660439-4636190af475')",
  }}
>
  <div className="absolute inset-0 bg-gradient-to-r from-black/70 to-transparent"></div>

  <div className="relative z-10 flex h-full items-center p-8 text-white">
    <div>
      <h1 className="text-4xl font-bold md:text-6xl">
        AI Technology
      </h1>

      <p className="mt-4 max-w-xl text-lg">
        Build powerful digital experiences with modern technology.
      </p>
    </div>
  </div>
</section>
```
### Tailwind Classes Used
relative → Creates positioning context.
bg-cover → Covers the hero section.
bg-center → Centers the background.
absolute inset-0 → Covers the complete hero.
bg-gradient-to-r → Creates a gradient overlay.
from-black/70 → Dark starting color.
to-transparent → Fades into transparency.
z-10 → Places content above the overlay.
items-center → Centers content vertically.

### What We Learned
How to create hero sections using background images.
How to use gradient overlays.
How to place readable text over images.
</details>

<details> <summary>13 — Build: AI-Tech Hero Section</summary>

### code
```tsx
<section
  className="relative min-h-[500px] bg-cover bg-center"
  style={{
    backgroundImage:
      "url('https://images.unsplash.com/photo-1518770660439-4636190af475')",
  }}
>
  <!-- Gradient Overlay -->
  <div className="absolute inset-0 bg-gradient-to-r from-black/80 via-black/50 to-transparent"></div>

  <!-- Hero Content -->
  <div className="relative z-10 flex min-h-[500px] items-center px-6 py-12 md:px-12 lg:px-20">

    <div className="max-w-2xl text-white">

      <span className="inline-block rounded-full bg-blue-500/80 px-4 py-2 text-sm font-semibold">
        AI TECHNOLOGY
      </span>

      <h1 className="mt-5 text-4xl font-bold md:text-6xl">
        Build the Future with AI
      </h1>

      <p className="mt-5 text-lg leading-8 text-gray-200 md:text-xl">
        Create smarter digital experiences with powerful artificial
        intelligence and modern technology.
      </p>

      <button className="mt-8 rounded-lg bg-blue-600 px-6 py-3 font-semibold text-white transition hover:bg-blue-700">
        Get Started
      </button>

    </div>
  </div>
</section>
```
### Tailwind Classes Used
relative → Creates the positioning context.
min-h-[500px] → Sets minimum hero height.
bg-cover → Makes the image cover the hero.
bg-center → Centers the background image.
absolute inset-0 → Creates the full overlay.
bg-gradient-to-r → Creates a horizontal gradient.
from-black/80 → Dark gradient starting point.
via-black/50 → Middle gradient color.
to-transparent → Fades the gradient.
relative z-10 → Places content above the overlay.
max-w-2xl → Limits text width.
md:text-6xl → Makes heading larger on medium screens.
hover:bg-blue-700 → Changes button color on hover.
transition → Makes the hover effect smooth.

### What We Learned
How to use background images in a hero section.
How to position and size background images.
How to create gradient overlays.
How to place content above an overlay.
How to create responsive hero content.
How to add a CTA button.
How to combine images, gradients, positioning, and responsive utilities into a complete UI section.
</details>













