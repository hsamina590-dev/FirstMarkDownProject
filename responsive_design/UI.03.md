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

### Code

```tsx
<h1 className="text-2xl md:text-4xl lg:text-6xl">
  Responsive Heading
</h1>
```
### Tailwind Classes Used
   *  Applying use class text-2xl → Default text size.
   -> md:text-4xl → Medium screen par larger text.
   -> lg:text-6xl → Large screen par even larger text.

### What We Learned
   * Text size ko different screen sizes ke according change kar sakte hain.
  -> md: medium screens ke liye hai.
  -> lg: large screens ke liye hai.

  </details>   
