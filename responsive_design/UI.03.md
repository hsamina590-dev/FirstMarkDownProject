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
)
}
```

### Tailwind Classes Used
   *  Applying use w-full p-4 text-center md:w-1/2 md:text-left
   *  Applying use class text-sm sm:text-lg

### What we Learn
  *  Mobile-first design means designing for small screens first.
     md: is used to change the design on medium and larger screens.
  * sm: changes the style for small screens and larger screens.
</details>
