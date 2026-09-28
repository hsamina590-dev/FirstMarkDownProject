# Tailwind CSS Practice

## Tailwind CSS my project test with Next.js

Tailwind CSS is already installed and `npm run dev` is working.

### This is a Tailwind CSS code block

<details>
<summary>01 — Layout Mastery</summary>

```tsx
export default function Home() {
  return (
    <div className="w-64 p-4 m-4 border-4 border-blue-500">
      CSS Box Model
    </div>
<div className="block">
    This is a block element
  </div>
<span className="inline">
    This is an inline element
  </span>
<div className="flex">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
  </div>
<div className="flex flex-row">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
  </div>
 <div className="flex flex-col">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
  </div>
 <div className="flex flex-wrap gap-4">
    <div className="w-32 p-4 bg-blue-500">Item 1</div>
    <div className="w-32 p-4 bg-green-500">Item 2</div>
    <div className="w-32 p-4 bg-red-500">Item 3</div>
    <div className="w-32 p-4 bg-yellow-500">Item 4</div>
  </div>
 <div className="flex justify-center">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
  </div>
  );
}
```

</details>

<details>
<summary>02 — Tailwind Classes Used</summary>

### Understand CSS Box Model through Tailwind
* The w-64 class sets the width.
  The p-4 class adds padding.
  The m-4 class adds margin.
  The border-4 class adds a border.

### Block code with Tailwind
* The class element block.

### Inline element
* The make element inline.

### flex items
* The class use flex-items.

### flex row
* The tailwind class flex flex-row.

### flex col
* The tailwind class flex flex-col.

### use flex wrap
* The flex flex-wrap gap-4.

### use justify
* The justify code justify-start, justify-end, justify-between, justify-around, justify-evenly. .






</details>

<details>
<summary>03 - What We Learned</summary>

### What we learn

* Applying CSS Box Model through Tailwind
  Applying width, padding, margin, border (Combining multiple Tailwind utilities)

* Applying class="block" element.

* Applying class="inline".

* Applying flex  → Makes the parent <div> a flex container.
  It places the child items in a row..

* flex → Makes the parent a flex container.
  flex-row → Places the items in a horizontal row.

* flex → Makes the parent a flex container.
  flex-col → Places the items in a vertical column.

* flex → Makes the parent a flex container.
  flex-wrap → Allows items to move to the next line when there is not enough space.
  gap-4 → Adds space between the items.

* justify-center → Centers the items horizontally.



</details>


















