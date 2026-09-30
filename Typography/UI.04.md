# Tailwind CSS Practice

## Typography

Typography in Tailwind CSS is used to control fonts, text size, weight, spacing, alignment, and text appearance.

---

<details>
<summary>01 — Font Family</summary>

### Code

```tsx
<p className="font-sans">
  This is a sans-serif font.
</p>
```

### Apply / Use Classes
** font-sans → Applies a sans-serif font.
** font-serif → Applies a serif font.
** font-mono → Applies a monospace font.

### What We Learned
** How to change the font family.
** How to use different font families with Tailwind CSS.
</details>

<details> <summary>02 — Font Size</summary>

### code

```tsx
<h1 className="text-4xl">
  Typography Heading
</h1>
```
### Apply / Use Classes
* text-sm
* text-lg
* text-2xl
* text-4xl

### What We Learned 
** How to change text size using Tailwind classes.
</details>

<details> <summary>03 — Font Weight</summary>

### code

```tsx
<h1 className="font-bold">
  Bold Heading
</h1>
```

### Apply / Use Classes
* font-normal
* font-medium
* font-semibold
* font-bold

### What We Learned
** How to make text normal, medium, semibold, or bold.
</details> 

<details> <summary>04 — Line Height</summary>

### code

```tsx
<p className="leading-8">
  This paragraph has increased line height.
</p>
```
### Apply / Use Classes
* leading-6
* leading-7
* leading-8
* leading-10

### What We Learned 
** How to control the vertical space between lines of text.
</details>

<details> <summary>05 — Letter Spacing</summary>

### code

```tsx
<p className="tracking-wide">
  Letter Spacing
</p>
```
### Apply / Use Classes
* tracking-tight
* tracking-normal
* tracking-wide
* tracking-wider
  
### What We Learned 
** How to increase or decrease space between letters.
</details>

<details> <summary>06 — Text Alignment</summary>

### code

```tsx
<p className="text-center">
  Centered Text
</p>
```
### Apply / Use Classes
* text-left
* text-center
* text-right
* text-justify
### What We Learned 
** How to align text horizontally.
</details>

<details> <summary>07 — Text Decoration</summary>

### code

```tsx
<p className="underline">
  Underlined Text
</p>
```

### Apply / Use Classes
* underline
* overline
* line-through
* no-underline
  
### What We Learned 
** How to add or remove text decorations.
</details>

<details> <summary>08 — Text Transformation</summary>

### code

```tsx
<p className="uppercase">
  text transformation
</p>
```

### Apply / Use Classes
* uppercase
* lowercase
* capitalize
* normal-case
  
### What We Learned 
** How to change the capitalization of text.
</details>

<details> <summary>09 — Text Truncation</summary>

### code

```tsx
<p className="truncate w-48">
  This is a very long text that will be truncated.
</p>
```

### Apply / Use Classes
* truncate
* text-ellipsis
* text-clip
  
### What We Learned 
** How to shorten overflowing text with Tailwind CSS.
</details>

<details> <summary>10 — Line Clamp</summary>

### code

```tsx
<p className="line-clamp-2">
  This is a long paragraph that will be limited to two lines of text.
</p>
```

### Apply / Use Classes
* line-clamp-1
* line-clamp-2
* line-clamp-3
  
### What We Learned 
** How to limit text to a specific number of lines.
</details>

<details> <summary>11 — Gradient Text</summary>

### code

```tsx
<h1 className="bg-gradient-to-r from-blue-500 to-purple-500 bg-clip-text text-transparent">
  Gradient Text
</h1>
```

### Apply / Use Classes
* bg-gradient-to-r
* from-blue-500
* to-purple-500
* bg-clip-text
* text-transparent
  
### What We Learned 
** How to create colorful gradient text using Tailwind CSS.
</details>

<details> <summary>12 — Responsive Typography</summary>

### code

```tsx
<h1 className="text-2xl md:text-4xl lg:text-6xl">
  Responsive Heading
</h1>
```

### Apply / Use Classes
* text-2xl
* md:text-4xl
* lg:text-6xl
  
### What We Learned 
** How to change text size according to screen size.
** How to use responsive typography.
</details>

<details> <summary>13 — Custom Google Fonts</summary>

<h1 className="font-sans">
  Custom Google Font
</h1>

### Apply / Use Classes
* Custom font configuration
* font-sans
  
### What We Learned
* How custom fonts can be added and used in a Tailwind project.
</details>

<details> <summary>14 — Custom Google Fonts</summary>

### code

```tsx
<h1 className="text-4xl font-bold">Main Heading</h1>

<h2 className="text-2xl font-semibold">Section Heading</h2>

<h3 className="text-xl font-medium">Sub Heading</h3>

<p className="text-base">
  Paragraph text.
</p>
```

### Apply / Use Classes
* text-4xl
* text-2xl
* text-xl
* font-bold
* font-semibold
* font-medium
* 
### What We Learned 
** How to create a clear heading hierarchy.
** How to make headings visually different from paragraphs.
</details>

<details> <summary>15 — Build a Professional Documentation Page</summary>

### code

```tsx
<article className="max-w-3xl mx-auto p-6">
  <h1 className="text-4xl font-bold">
    Tailwind CSS Documentation
  </h1>

  <p className="mt-4 text-lg leading-8 text-gray-600">
    Learn Tailwind CSS typography utilities.
  </p>

  <h2 className="mt-8 text-2xl font-semibold">
    Typography
  </h2>

  <p className="mt-4 leading-7">
    Tailwind CSS provides utilities for styling text and fonts.
  </p>
</article>
```

### Apply / Use Classes
* max-w-3xl
* mx-auto
* p-6
* text-4xl
* font-bold
* text-lg
* leading-8
* text-2xl
* font-semibold
  
### What We Learned 
** How to build a professional documentation/article page.
** How to combine headings, paragraphs, spacing, and typography utilities. 
</details>

## Typography file 

01 Font Family
→
02 Font Size
→
03 Font Weight
→
...
→
15 Professional Documentation Page
and topic = separate dropdown + Code + Apply/Use Classes + What We Learned.














