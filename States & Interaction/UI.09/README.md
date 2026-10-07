
# Tailwind CSS Practice

## States & Interaction

Tailwind CSS state variants allow us to change the appearance and behavior of elements when users interact with them.

---

<details>
<summary>01 — hover:</summary>

### Code

```tsx
<button className="rounded-lg bg-blue-500 px-5 py-3 text-white hover:bg-blue-700">
  Hover Me
</button>
```
### Tailwind Classes Used
hover:bg-blue-700 → Changes the background when the mouse is over the button.
bg-blue-500 → Normal background color.
text-white → White text.

### What We Learned
hover: applies styles when the user moves the mouse over an element.
It is commonly used for buttons, links, and cards.
</details>

<details> <summary>02 — focus:</summary>

### Code

```tsx
<input
  type="text"
  placeholder="Enter your name"
  className="rounded-lg border border-gray-300 p-3 focus:border-blue-500 focus:ring-2 focus:ring-blue-300"
/>
```
### Tailwind Classes Used
focus:border-blue-500 → Changes the border when the input is focused.
focus:ring-2 → Adds a focus ring.
focus:ring-blue-300 → Sets the ring color.

### What We Learned
focus: applies styles when an input or button receives focus.
Focus styles make forms easier to use.
</details>

<details> <summary>03 — active:</summary>

### code
```tsx
<button className="rounded-lg bg-blue-500 px-5 py-3 text-white active:bg-blue-900">
  Click Me
</button>
```
### Tailwind Classes Used
active:bg-blue-900 → Changes the background while the button is being clicked.
bg-blue-500 → Normal background.
text-white → Text color.

### What We Learned
active: applies styles while an element is being pressed.
It helps give visual feedback during interaction.
</details>

<details> <summary>04 — visited:</summary>

### code
```tsx
<a
  href="https://example.com"
  className="text-blue-500 visited:text-purple-600"
>
  Visit Website
</a>
```
### Tailwind Classes Used
text-blue-500 → Normal link color.
visited:text-purple-600 → Changes the color after the link has been visited.

### What We Learned
visited: styles links that the user has already visited.
</details>

<details> <summary>05 — disabled:</summary>

### code
```tsx
<button
  disabled
  className="rounded-lg bg-blue-500 px-5 py-3 text-white disabled:cursor-not-allowed disabled:opacity-50"
>
  Disabled Button
</button>
```
### Tailwind Classes Used
disabled:opacity-50 → Makes the button semi-transparent.
disabled:cursor-not-allowed → Shows a disabled cursor.
bg-blue-500 → Normal background.

### What We Learned
disabled: applies styles when an element is disabled.
It helps users understand that an action cannot currently be performed.
</details>

<details> <summary>06 — checked:</summary>

### code
```tsx
<label className="flex items-center gap-2">
  <input
    type="checkbox"
    defaultChecked
    className="accent-blue-500"
  />

  <span>Accept Terms</span>
</label>
```
### Tailwind Classes Used
accent-blue-500 → Changes the checkbox accent color.
flex → Creates a flex layout.
items-center → Aligns items vertically.
gap-2 → Adds space between the checkbox and text.

### What We Learned
Checkbox and radio states can be styled when they are checked.
The checked state represents a selected form control.
</details>

<details> <summary>07 — group-hover:</summary>

### code
```tsx
<div className="group w-64 rounded-xl bg-gray-100 p-6">
  <h2 className="text-xl font-bold group-hover:text-blue-600">
    Hover the Card
  </h2>

  <p className="mt-2 group-hover:text-gray-700">
    The text changes when the card is hovered.
  </p>
</div>
```
### Tailwind Classes Used
group → Creates a group for child state styling.
group-hover:text-blue-600 → Changes the heading color when the parent is hovered.
group-hover:text-gray-700 → Changes the paragraph color on parent hover.

### What We Learned
group-hover: allows child elements to react when the parent is hovered.
It is useful for interactive cards.
</details>

<details> <summary>08 — group-focus:</summary>

### code
```tsx
<div className="group w-64 rounded-xl border p-6">
  <button className="rounded-lg bg-blue-500 px-4 py-2 text-white group-focus:text-yellow-300">
    Focus Button
  </button>
</div>
```
### Tailwind Classes Used
group → Creates a group.
group-focus: → Allows child elements to react to a focus state.

### What We Learned
group-focus: can be used when interaction with a grouped element needs to affect another element.
</details>

<details> <summary>09 — peer</summary>

### code
```tsx
<div>
  <input
    type="checkbox"
    id="show"
    className="peer"
  />

  <label
    htmlFor="show"
    className="ml-2 text-gray-500 peer-checked:text-blue-600"
  >
    Accept Terms
  </label>
</div>
```
### Tailwind Classes Used
peer → Marks an element as a peer.
peer-checked:text-blue-600 → Changes the label when the checkbox is checked.

### What We Learned
peer allows one element to react to the state of another sibling element.
It is useful for checkboxes, radio buttons, and custom form controls.
</details>

<details> <summary>10 — peer-*</summary>

### code
```tsx
<div>
  <input
    type="checkbox"
    id="status"
    className="peer"
  />

  <span className="ml-2 text-gray-500 peer-checked:text-green-600">
    Selected
  </span>
</div>
```
### Tailwind Classes Used
peer → Creates a peer element.
peer-checked: → Reacts when the peer is checked.
text-green-600 → Changes the text color.

### What We Learned
peer-* variants allow elements to respond to different states of a sibling.
Examples include peer-checked, peer-focus, and peer-disabled.
</details>

<details> <summary>11 — Focus-visible States</summary>

### code
```tsx
<button className="rounded-lg px-5 py-3 focus-visible:outline-none focus-visible:ring-4 focus-visible:ring-blue-300">
  Focus Visible
</button>
```
### Tailwind Classes Used
focus-visible:outline-none → Removes the default outline when focus is visible.
focus-visible:ring-4 → Adds a visible focus ring.
focus-visible:ring-blue-300 → Sets the ring color.

### What We Learned
focus-visible: applies styles when focus should be visually indicated.
It helps improve keyboard accessibility.
</details>

<details> <summary>12 — Button Interaction States</summary>

### code
```tsx
<button
  className="
    rounded-lg bg-blue-500 px-6 py-3 text-white
    transition
    hover:bg-blue-700
    active:bg-blue-900
    focus:outline-none
    focus:ring-4
    focus:ring-blue-300
    disabled:cursor-not-allowed
    disabled:opacity-50
  "
>
  Interactive Button
</button>
```
### Tailwind Classes Used
hover: → Hover state.
active: → Click/press state.
focus: → Focus state.
disabled: → Disabled state.
transition → Makes state changes smoother.

### What We Learned
A button can have multiple interaction states.
Tailwind allows all these states to be combined in one class list.
</details>

<details> <summary>13 — Form Interaction States</summary>

### code
```tsx
<div className="max-w-md">
  <label className="mb-2 block font-medium">
    Email
  </label>

  <input
    type="email"
    placeholder="Enter your email"
    className="
      w-full rounded-lg border border-gray-300 p-3
      transition
      hover:border-gray-400
      focus:border-blue-500
      focus:ring-4
      focus:ring-blue-100
      invalid:border-red-500
      invalid:ring-red-100
    "
  />
</div>
```
### Tailwind Classes Used
hover:border-gray-400 → Changes border on hover.
focus:border-blue-500 → Changes border on focus.
focus:ring-4 → Adds focus ring.
invalid:border-red-500 → Changes border when input is invalid.
invalid:ring-red-100 → Adds invalid state ring.

### What We Learned
Form fields can have hover, focus, and invalid states.
State variants help users understand what is happening with a form field.
</details>

<details> <summary>14 — Card Hover Effects</summary>
  
### code
```tsx
<div className="group max-w-sm rounded-xl bg-white p-6 shadow-md transition duration-300 hover:-translate-y-2 hover:shadow-xl">
  <h2 className="text-2xl font-bold transition group-hover:text-blue-600">
    Product Card
  </h2>

  <p className="mt-2 text-gray-600">
    Hover over this card to see the effect.
  </p>

  <button className="mt-4 rounded-lg bg-blue-500 px-4 py-2 text-white group-hover:bg-blue-700">
    View Product
  </button>
</div>
```
### Tailwind Classes Used
group → Creates a group.
hover:-translate-y-2 → Moves the card upward on hover.
hover:shadow-xl → Increases the shadow.
group-hover:text-blue-600 → Changes heading color.
group-hover:bg-blue-700 → Changes button color.
transition → Smooth transition effect.

### What We Learned
Hover effects can make cards more interactive.
group-hover: allows multiple child elements to react to the card hover.
transition makes the animation smoother.
</details>

<details> <summary>15 — Build: Interactive Login Form</summary>

### code
```tsx
<div className="mx-auto max-w-md rounded-2xl bg-white p-8 shadow-xl">

  <h1 className="text-3xl font-bold text-gray-900">
    Login
  </h1>

  <p className="mt-2 text-gray-500">
    Welcome back! Please login to your account.
  </p>

  <form className="mt-6 space-y-5">

    <div>
      <label
        htmlFor="email"
        className="mb-2 block font-medium text-gray-700"
      >
        Email
      </label>

      <input
        id="email"
        type="email"
        placeholder="Enter your email"
        className="
          w-full rounded-lg border border-gray-300 p-3
          transition
          hover:border-gray-400
          focus:border-blue-500
          focus:outline-none
          focus:ring-4
          focus:ring-blue-100
          invalid:border-red-500
        "
      />
    </div>

    <div>
      <label
        htmlFor="password"
        className="mb-2 block font-medium text-gray-700"
      >
        Password
      </label>

      <input
        id="password"
        type="password"
        placeholder="Enter your password"
        className="
          w-full rounded-lg border border-gray-300 p-3
          transition
          hover:border-gray-400
          focus:border-blue-500
          focus:outline-none
          focus:ring-4
          focus:ring-blue-100
          invalid:border-red-500
        "
      />
    </div>

    <label className="flex items-center gap-2">
      <input
        type="checkbox"
        className="accent-blue-600"
      />

      <span className="text-sm text-gray-600">
        Remember me
      </span>
    </label>

    <button
      type="submit"
      className="
        w-full rounded-lg bg-blue-600 py-3
        font-semibold text-white
        transition
        hover:bg-blue-700
        active:bg-blue-800
        focus:outline-none
        focus-visible:ring-4
        focus-visible:ring-blue-300
      "
    >
      Login
    </button>

    <button
      type="button"
      disabled
      className="
        w-full rounded-lg bg-gray-300 py-3
        font-semibold text-gray-500
        disabled:cursor-not-allowed
        disabled:opacity-50
      "
    >
      Disabled Button
    </button>

  </form>

  <p className="mt-6 text-center text-sm text-gray-500">
    Don't have an account?
    <a
      href="#"
      className="ml-1 text-blue-600 hover:text-blue-800"
    >
      Register
    </a>
  </p>

</div>
```
### Tailwind Classes Used
hover: → Hover interaction.
focus: → Focus interaction.
focus-visible: → Keyboard-visible focus state.
active: → Active/click state.
disabled: → Disabled button state.
invalid: → Invalid form input state.
accent-blue-600 → Checkbox color.
transition → Smooth interaction effects.
ring-* → Focus indication.
group-hover: → Child element interaction through parent hover.
peer-* → Interaction based on a sibling element.

### What We Learned
How to create hover states.
How to create focus states.
How to create active states.
How to style disabled elements.
How to style checked form controls.
How group-hover: works.
How peer-* variants work.
How to create accessible focus-visible states.
How to create interactive form fields.
How to combine different interaction states in a complete login UI.
</details>
