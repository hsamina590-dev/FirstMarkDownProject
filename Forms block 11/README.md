# Tailwind CSS Practice

## Forms

Tailwind CSS provides utility classes for styling form elements such as
inputs, selects, checkboxes, radio buttons, textareas, and validation states.

---

<details>
<summary>01 — Input Styling</summary>

### Code

```tsx
<input
  type="text"
  placeholder="Enter your name"
  className="w-full rounded-lg border border-gray-300 p-3"
/>

### Tailwind Class
w-full rounded-lg border border-gray-300 p-3

### ↓ We Learn
Input ko width, border, rounded corners aur padding dene ke liye Tailwind classes use karte hain.

</details>

<details> <summary>02 — Select Styling</summary>
  
### Code
<select className="w-full rounded-lg border border-gray-300 p-3">
  <option>Select your city</option>
  <option>Pakpattan</option>
  <option>Lahore</option>
  <option>Islamabad</option>
</select>
Tailwind Class

rounded-lg border p-3

↓ We Learn

select dropdown ko border, rounded corners aur spacing ke saath style karna seekha.

</details>
<details> <summary>03 — Checkbox Styling</summary>
Code
<label className="flex items-center gap-2">
  <input
    type="checkbox"
    className="h-5 w-5 accent-blue-500"
  />
  <span>I agree to the terms</span>
</label>
Tailwind Class

h-5 w-5 accent-blue-500

↓ We Learn

Checkbox ka size aur checked hone par color accent-blue-500 se control kar sakte hain.

</details>
<details> <summary>04 — Radio Styling</summary>
Code
<div className="flex gap-4">
  <label className="flex items-center gap-2">
    <input
      type="radio"
      name="gender"
      className="h-5 w-5 accent-blue-500"
    />
    Male
  </label>

  <label className="flex items-center gap-2">
    <input
      type="radio"
      name="gender"
      className="h-5 w-5 accent-blue-500"
    />
    Female
  </label>
</div>
Tailwind Class

h-5 w-5 accent-blue-500

↓ We Learn

Radio buttons ko size aur accent color de kar style kar sakte hain.

</details>
<details> <summary>05 — Textarea Styling</summary>
Code
<textarea
  rows={4}
  placeholder="Write your message..."
  className="w-full rounded-lg border border-gray-300 p-3"
></textarea>
Tailwind Class

w-full rounded-lg border p-3

↓ We Learn

Textarea ko full width, border, rounded corners aur padding ke saath style karna seekha.

</details>
<details> <summary>06 — Placeholder Styling</summary>
Code
<input
  type="text"
  placeholder="Enter your email"
  className="w-full rounded-lg border p-3 placeholder:text-gray-400"
/>
Tailwind Class

placeholder:text-gray-400

↓ We Learn

placeholder: variant se placeholder text ka color aur doosri properties change kar sakte hain.

</details>
<details> <summary>07 — Focus Styling</summary>
Code
<input
  type="text"
  placeholder="Click here"
  className="w-full rounded-lg border border-gray-300 p-3 outline-none focus:border-blue-500 focus:ring-2 focus:ring-blue-200"
/>
Tailwind Class

focus:border-blue-500
focus:ring-2
focus:ring-blue-200

↓ We Learn

Jab user input par click karta hai to focus: classes apply hoti hain.

Is se user ko pata chalta hai ke currently kaunsa field active hai.

</details>
<details> <summary>08 — Error States</summary>
Code
<div>
  <input
    type="email"
    placeholder="Enter your email"
    className="w-full rounded-lg border border-red-500 p-3 outline-none focus:ring-2 focus:ring-red-200"
  />

  <p className="mt-1 text-sm text-red-500">
    Please enter a valid email.
  </p>
</div>
Tailwind Class

border-red-500
text-red-500
focus:ring-red-200

↓ We Learn

Error state mein input ka border aur error message red color mein show kar sakte hain.

</details>
<details> <summary>09 — Success States</summary>
Code
<div>
  <input
    type="email"
    value="samina@example.com"
    readOnly
    className="w-full rounded-lg border border-green-500 p-3 outline-none focus:ring-2 focus:ring-green-200"
  />

  <p className="mt-1 text-sm text-green-600">
    Email is valid.
  </p>
</div>
Tailwind Class

border-green-500
text-green-600
focus:ring-green-200

↓ We Learn

Success state mein green border aur success message use karte hain.

</details>
<details> <summary>10 — Disabled States</summary>
Code
<button
  disabled
  className="cursor-not-allowed rounded-lg bg-gray-300 px-5 py-2 text-gray-500"
>
  Submit
</button>
Tailwind Class

disabled:
cursor-not-allowed

↓ We Learn

Disabled element ko user click nahi kar sakta.

cursor-not-allowed user ko indicate karta hai ke button disabled hai.

</details>
<details> <summary>11 — Form Layouts</summary>
Code
<form className="mx-auto max-w-md space-y-4">

  <div>
    <label className="mb-1 block font-medium">
      Name
    </label>

    <input
      type="text"
      placeholder="Enter your name"
      className="w-full rounded-lg border p-3"
    />
  </div>

  <div>
    <label className="mb-1 block font-medium">
      Email
    </label>

    <input
      type="email"
      placeholder="Enter your email"
      className="w-full rounded-lg border p-3"
    />
  </div>

  <button
    type="submit"
    className="w-full rounded-lg bg-blue-500 px-5 py-3 text-white"
  >
    Submit
  </button>

</form>
Tailwind Class

max-w-md
space-y-4
block
w-full

↓ We Learn

Form layout mein space-y-4 fields ke darmiyan vertical spacing create karta hai.

max-w-md form ki maximum width control karta hai.

</details>
<details> <summary>12 — Responsive Forms</summary>
Code
<form className="mx-auto grid max-w-3xl grid-cols-1 gap-4 p-4 md:grid-cols-2">

  <input
    type="text"
    placeholder="First Name"
    className="rounded-lg border p-3"
  />

  <input
    type="text"
    placeholder="Last Name"
    className="rounded-lg border p-3"
  />

  <input
    type="email"
    placeholder="Email"
    className="rounded-lg border p-3"
  />

  <input
    type="tel"
    placeholder="Phone"
    className="rounded-lg border p-3"
  />

  <textarea
    placeholder="Message"
    rows={4}
    className="rounded-lg border p-3 md:col-span-2"
  ></textarea>

  <button
    type="submit"
    className="rounded-lg bg-blue-500 px-5 py-3 text-white md:col-span-2"
  >
    Submit
  </button>

</form>
Tailwind Class

grid-cols-1
md:grid-cols-2
md:col-span-2

↓ We Learn

Mobile par form single column mein hota hai.

md:grid-cols-2 ki wajah se medium screen aur us se badi screen par form 2 columns mein show hota hai.

</details>
<details> <summary>13 — Build: Complete Registration Form</summary>
Code
<form className="mx-auto max-w-lg space-y-5 rounded-xl border p-6 shadow-md">

  <h2 className="text-2xl font-bold">
    Create Account
  </h2>

  <div>
    <label className="mb-1 block font-medium">
      Name
    </label>

    <input
      type="text"
      placeholder="Enter your name"
      className="w-full rounded-lg border border-gray-300 p-3 outline-none focus:border-blue-500 focus:ring-2 focus:ring-blue-200"
    />
  </div>


  <div>
    <label className="mb-1 block font-medium">
      Email
    </label>

    <input
      type="email"
      placeholder="Enter your email"
      className="w-full rounded-lg border border-red-500 p-3 outline-none focus:ring-2 focus:ring-red-200"
    />

    <p className="mt-1 text-sm text-red-500">
      Please enter a valid email.
    </p>
  </div>


  <div>
    <label className="mb-1 block font-medium">
      Password
    </label>

    <input
      type="password"
      placeholder="Enter your password"
      className="w-full rounded-lg border border-gray-300 p-3 outline-none focus:border-blue-500 focus:ring-2 focus:ring-blue-200"
    />
  </div>


  <div>
    <label className="mb-1 block font-medium">
      City
    </label>

    <select className="w-full rounded-lg border border-gray-300 p-3">
      <option>Select your city</option>
      <option>Pakpattan</option>
      <option>Lahore</option>
      <option>Islamabad</option>
    </select>
  </div>


  <div className="flex items-center gap-2">
    <input
      type="checkbox"
      className="h-5 w-5 accent-blue-500"
    />

    <span className="text-sm">
      I agree to the terms and conditions.
    </span>
  </div>


  <button
    type="submit"
    className="w-full rounded-lg bg-blue-500 px-5 py-3 font-medium text-white transition-colors duration-300 hover:bg-blue-700"
  >
    Create Account
  </button>

</form>
Tailwind Class

border
rounded-lg
p-3
focus:
placeholder:
accent-blue-500
space-y-5
w-full
transition-colors
hover:bg-blue-700

↓ We Learn

Is build mein humne complete registration form banaya.

Input styling
Select styling
Checkbox styling
Password field
Focus state
Error state
Form spacing
Button hover effect
Responsive-friendly width
Build

Complete registration form with validation-state UI.

</details> ```

## Block 11  flow:
Input → Select → Checkbox → Radio → Textarea → Placeholder → Focus → Error → Success → Disabled → Form Layout → Responsive Form → Build




















