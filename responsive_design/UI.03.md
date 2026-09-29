# Tailwind CSS Practice

## Responsive Design

Tailwind CSS responsive design allows us to create layouts that work on mobile, tablet, and desktop screens.

<details>
<summary>01 — Mobile First & Breakpoints</summary>

### Understand Mobile-First Design

#### Code

```tsx
export default function Home(){
return(
<div className="w-full p-4 text-center md:w-1/2 md:text-left">
  Mobile First Design
</div>
<div className="text-sm sm:text-lg">
  Responsive Text
</div>
<div className="text-base md:text-2xl">
  Responsive Text
</div>
<div className="text-lg lg:text-3xl">
  Responsive Text
</div>
<div className="text-xl xl:text-4xl">
  Responsive Text
</div>
<div className="text-2xl 2xl:text-5xl">
  Responsive Text
</div>
)
}
```

### Tailwind Classes Used
   *  Applying use w-full p-4 text-center md:w-1/2 md:text-left
   *  Applying use class text-sm sm:text-lg
   *  Applying use class text-base md:text-2xl
   *  Applying use class text-lg lg:text-3xl
   *  Applying use class text-xl xl:text-4xl
   *  Applying use class text-2xl 2xl:text-5xl


### What we Learn
  *  Mobile-first design means designing for small screens first.
     md: is used to change the design on medium and larger screens.
  * sm: changes the style for small screens and larger screens.
    
</details>

<details>
<summary>02 — Change Typography Responsively</summary>

### Change Spacing Responsively
### Change Layout Responsively
### Hide/Show Elements Responsively

### Code

```tsx
<h1 className="text-2xl md:text-4xl lg:text-6xl">
  Responsive Heading
</h1>
<div className="p-4 md:p-8 lg:p-12">
  Responsive Spacing
</div>
<div className="flex flex-col md:flex-row">
  <div>Item 1</div>
  <div>Item 2</div>
</div>
<div className="block md:hidden">
  Mobile Only
</div>
```
### Tailwind Classes Used
   *  Applying use class text-2xl → Default text size.
   * md:text-4xl → Medium screen par larger text.
   * lg:text-6xl → Large screen par even larger text.
   * flex-col md:flex-row
   * block md:hidden

### What We Learned
   * Change font size according to screen size.
   * Change padding according to screen size.
   * Change layout direction responsively.
   * Hide and show elements on different screens.

  </details> 

  <details>
<summary>03 — Responsive Flex & Grid</summary>

### Change Grid Columns Responsively
### Change Flex Direction Responsively
### Build Responsive Cards

### Code

```tsx
<div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>
<div className="flex flex-col md:flex-row gap-4">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>
<div className="grid grid-cols-1 md:grid-cols-3 gap-4">
  <div className="p-6 border rounded">Card 1</div>
  <div className="p-6 border rounded">Card 2</div>
  <div className="p-6 border rounded">Card 3</div>
</div>

```
### Tailwind Classes Used
   *  Applying class use grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4
   *  Applying class use flex flex-col md:flex-row gap-4
   *  Applying class use grid grid-cols-1 md:grid-cols-3 gap-4

### What We Learned
   * Change font size according to screen size.
   * Change padding according to screen size.
   * Change layout direction responsively.
   * Hide and show elements on different screens.

  </details>   

