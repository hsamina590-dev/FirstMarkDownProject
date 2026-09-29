# Tailwind CSS Practice

## Responsive Design

Tailwind CSS responsive design allows us to create layouts that work on mobile, tablet, and desktop screens.

### Understand Mobile-First Design

<details>
<summary>01 — Change Spacing Responsively </summary>

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
<h2>Change Grid Columns Responsively</h2>
<div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>

<h2>Change Flex Direction Responsively</h2>
<div className="flex flex-col md:flex-row gap-4">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>

<h2>Build Responsive Cards</h2>
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

<details> <summary>04 — Responsive Components & Landing Page</summary>
  
### Build Mobile Navigation
### Build Responsive Tables
### Build Responsive Hero Section
### Build a Complete Responsive Landing Page
### code
```tsx
<nav className="flex flex-col md:flex-row gap-4">
  <a href="#">Home</a>
  <a href="#">About</a>
  <a href="#">Contact</a>
</nav>

<h2>Build Responsive Tables</h2>
<div className="overflow-x-auto">
  <table className="min-w-full">
    <tbody>
      <tr>
        <td className="p-4">Name</td>
        <td className="p-4">Email</td>
      </tr>
    </tbody>
  </table>
</div>

<h2>Build Responsive Hero Section</h2>
<section className="p-6 md:p-12 lg:p-20 text-center">
  <h1 className="text-3xl md:text-5xl lg:text-6xl font-bold">
    Welcome to Our Website
  </h1>
  <p className="mt-4 text-base md:text-lg">
    A responsive hero section.
  </p>
</section>

<h2>Build a Complete Responsive Landing Page</h2>
<div className="min-h-screen">
  <header className="p-4 md:p-6">
    <h1 className="text-2xl md:text-4xl font-bold">
      My Website
    </h1>
  </header>

  <main className="grid grid-cols-1 md:grid-cols-2 gap-6 p-6">
    <div>
      <h2 className="text-3xl md:text-5xl font-bold">
        Responsive Design
      </h2>
      <p className="mt-4">
        Mobile to desktop responsive layout.
      </p>
    </div>

    <div className="p-6 border rounded">
      Responsive Content
    </div>
  </main>
</div>
```

## What We Learned
* Build mobile navigation.
* Build responsive cards.
* Build responsive tables.
* Build responsive hero sections.
* Build a complete responsive landing page.
</details>
  

