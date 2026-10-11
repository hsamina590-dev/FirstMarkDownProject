# UI 17 — Personal Portfolio Website

This project is a personal portfolio website built with Next.js, React, TypeScript, and Tailwind CSS.

## Project Overview

* Personal introduction
* Skills and technologies
* Featured projects
* Contact section
* Responsive layout

<details>
<summary>01 — Project Data (Projects & Skills)</summary>

  ### code
  
const projects = [
  {
    number: "01",
    title: "WeatherNow",
    description: "A weather website using the Open-Meteo API.",
    tags: ["Next.js", "API", "Tailwind CSS"],
  },
];

const skills = ["HTML", "CSS", "JavaScript", "React", "Next.js"];

### Tailwind Classes

text-cyan-400 → cyan text color

font-bold → bold text

flex → flexbox layout

gap-4 → space between items

### What We Learned

How to store project information in arrays.

How to organize skills and project data.

How to reuse data in React components.

</details>

<details>
<summary>02 — Navbar & Navigation</summary>

### Code
```tsx
<header className="sticky top-0 z-50 border-b border-white/10 bg-slate-950/95">
  <nav className="mx-auto flex max-w-6xl items-center justify-between px-6 py-5">
    <a href="#home" className="text-2xl font-bold tracking-tight">
      Samina<span className="text-cyan-400">.dev</span>
    </a>

    <div className="flex flex-wrap gap-4 text-sm text-slate-300">
      <a href="#about" className="hover:text-cyan-400">About</a>
      <a href="#skills" className="hover:text-cyan-400">Skills</a>
      <a href="#projects" className="hover:text-cyan-400">Projects</a>
      <a href="#contact" className="hover:text-cyan-400">Contact</a>
    </div>
  </nav>
</header>
```
### Tailwind Classes

sticky top-0 → navbar stays at the top while scrolling.

z-50 → places the navbar above other content.

max-w-6xl mx-auto → limits width and centers content.

justify-between → places items at opposite ends.

hover:text-cyan-400 → changes text color on hover.

### What We Learned

How to create a navigation bar.

How to link sections using IDs.

How to use hover effects and sticky positioning.

</details>

      {/* Hero Section */}
      
     <details>
     
<summary>03 — Hero Section</summary>

### Code

```tsx
{/* Hero Section */}
<section
  id="home"
  className="mx-auto grid max-w-6xl items-center gap-12 px-6 py-24 md:grid-cols-2 md:py-32"
>
  <div>
    <p className="mb-5 font-medium text-cyan-400">
      HELLO, WELCOME TO MY PORTFOLIO
    </p>

    <h1 className="text-4xl font-bold leading-tight sm:text-5xl lg:text-6xl">
      I build modern
      <span className="block text-cyan-400">
        digital experiences.
      </span>
    </h1>

    <p className="mt-6 max-w-lg leading-7 text-slate-400">
      Hi, I am Samina. I am learning web development and
      building modern websites using React, Next.js, and
      Tailwind CSS. I enjoy turning ideas into real projects.
    </p>

    <div className="mt-8 flex flex-wrap gap-4">
      <a
        href="#projects"
        className="rounded-lg bg-cyan-400 px-6 py-3 font-semibold text-slate-950 transition hover:bg-cyan-300"
      >
        View My Work
      </a>

      <a
        href="#contact"
        className="rounded-lg border border-slate-600 px-6 py-3 font-semibold transition hover:border-cyan-400"
      >
        Contact Me
      </a>
    </div>
  </div>

  <div className="flex justify-center">
    <div className="flex h-64 w-64 items-center justify-center rounded-full border border-cyan-400/40 bg-gradient-to-br from-cyan-400/20 to-blue-600/20 shadow-2xl shadow-cyan-500/10 sm:h-80 sm:w-80">
      <div className="flex h-52 w-52 items-center justify-center rounded-full border border-white/10 bg-slate-900 sm:h-64 sm:w-64">
        <span className="text-7xl font-bold text-cyan-400 sm:text-8xl">
          S
        </span>
      </div>
    </div>
  </div>
</section>
```

↓

### Tailwind Classes

| Tailwind Class | What It Does |
|---|---|
| `mx-auto` | Centers the section horizontally. |
| `grid` | Creates a CSS Grid layout. |
| `max-w-6xl` | Limits the maximum width. |
| `items-center` | Aligns grid items vertically in the center. |
| `gap-12` | Adds space between grid items. |
| `px-6` | Adds horizontal padding. |
| `py-24` | Adds vertical padding. |
| `md:grid-cols-2` | Displays two columns on medium screens and larger. |
| `font-medium` | Applies medium font weight. |
| `text-cyan-400` | Applies cyan text color. |
| `text-4xl` | Sets a large heading size. |
| `font-bold` | Makes text bold. |
| `leading-tight` | Reduces the space between lines. |
| `sm:text-5xl` | Increases heading size on small screens and larger. |
| `lg:text-6xl` | Uses a larger heading on large screens and larger. |
| `block` | Displays the span on a new line. |
| `mt-6` | Adds top margin. |
| `max-w-lg` | Limits the paragraph width. |
| `leading-7` | Sets line height. |
| `text-slate-400` | Applies muted gray text color. |
| `flex` | Creates a Flexbox layout. |
| `flex-wrap` | Allows items to move to the next line. |
| `justify-center` | Centers items horizontally. |
| `rounded-lg` | Adds rounded corners. |
| `bg-cyan-400` | Applies a cyan background. |
| `px-6 py-3` | Adds horizontal and vertical padding. |
| `transition` | Animates supported property changes. |
| `hover:bg-cyan-300` | Changes the background on hover. |
| `border` | Adds a border. |
| `border-slate-600` | Applies a slate-colored border. |
| `hover:border-cyan-400` | Changes the border color on hover. |
| `h-64 w-64` | Sets height and width. |
| `rounded-full` | Creates a circular shape when dimensions are equal. |
| `border-cyan-400/40` | Applies a cyan border at 40% opacity. |
| `bg-gradient-to-br` | Creates a gradient from top-left to bottom-right. |
| `from-cyan-400/20` | Sets the gradient's starting color. |
| `to-blue-600/20` | Sets the gradient's ending color. |
| `shadow-2xl` | Adds a large shadow. |
| `shadow-cyan-500/10` | Gives the shadow a cyan tint with 10% opacity. |
| `sm:h-80 sm:w-80` | Increases the circle's dimensions at the `sm` breakpoint. |
| `text-7xl sm:text-8xl` | Makes the letter S larger on small screens and larger. |

↓

### What We Learned

- How to create a Hero Section for a personal portfolio.
- How to use CSS Grid to create a two-column layout.
- How to make the layout responsive using breakpoints.
- How to style headings and paragraphs with typography utilities.
- How to create buttons with hover effects.
- How to build circular elements using `rounded-full`.
- How to use gradient backgrounds and shadows.
- How to connect buttons to other page sections using `href`.
- How to create a professional portfolio introduction.

</details>

      {/* About Section */}

 <details>
   
<summary>04 — About Section</summary>

### Code

```tsx
{/* About Section */}
<section
  id="about"
  className="border-y border-white/10 bg-slate-900/60"
>
  <div className="mx-auto max-w-6xl px-6 py-20">
    <p className="font-semibold text-cyan-400">
      GET TO KNOW ME
    </p>

    <h2 className="mt-3 text-3xl font-bold sm:text-4xl">
      About Me
    </h2>

    <p className="mt-6 max-w-3xl leading-8 text-slate-400">
      I enjoy learning web development and turning ideas into
      practical websites. My focus is on writing clean code,
      building responsive layouts, and improving my skills
      through real-world projects.
    </p>
  </div>
</section>
```

↓

### Tailwind Classes

| Tailwind Class | What It Does |
|---|---|
| `border-y` | Adds borders to the top and bottom. |
| `border-white/10` | Applies a white border with 10% opacity. |
| `bg-slate-900/60` | Adds a dark slate background with 60% opacity. |
| `mx-auto` | Centers the container horizontally. |
| `max-w-6xl` | Limits the maximum width of the container. |
| `px-6` | Adds horizontal padding. |
| `py-20` | Adds vertical padding. |
| `font-semibold` | Applies a semibold font weight. |
| `text-cyan-400` | Changes the text color to cyan. |
| `mt-3` | Adds top margin. |
| `text-3xl` | Sets the heading font size to 3XL. |
| `font-bold` | Makes the heading bold. |
| `sm:text-4xl` | Increases the heading size at the `sm` breakpoint and above. |
| `mt-6` | Adds top margin to the paragraph. |
| `max-w-3xl` | Limits the paragraph's maximum width. |
| `leading-8` | Sets the line height to create comfortable paragraph spacing. |
| `text-slate-400` | Applies a muted slate-gray text color. |

↓

### What We Learned

- How to create an About section for a personal portfolio.
- How to use `id="about"` to identify a page section.
- How to add top and bottom borders using `border-y`.
- How to apply a dark background with opacity.
- How to center content and control its maximum width.
- How to style headings using font size and font weight.
- How to improve paragraph readability with `leading-8`.
- How to make heading sizes responsive using `sm:text-4xl`.
- How to create a clean and professional About Me section.

</details>

      {/* Skills Section */}

<details>
<summary>05 — Skills Section</summary>

### Code

```tsx
{/* Skills Section */}
<section id="skills" className="mx-auto max-w-6xl px-6 py-20">
  <p className="font-semibold text-cyan-400">MY TOOLKIT</p>

  <h2 className="mt-3 text-3xl font-bold sm:text-4xl">
    Skills & Technologies
  </h2>

  <div className="mt-8 flex flex-wrap gap-3">
    {skills.map((skill) => (
      <span
        key={skill}
        className="rounded-lg border border-slate-700 bg-slate-900 px-5 py-3 text-slate-300 transition hover:border-cyan-400 hover:text-cyan-400"
      >
        {skill}
      </span>
    ))}
  </div>
</section>
```

↓

### Tailwind Classes

| Tailwind Class | What It Does |
|---|---|
| `mx-auto` | Centers the section horizontally. |
| `max-w-6xl` | Limits the maximum width. |
| `px-6 py-20` | Adds horizontal and vertical padding. |
| `font-semibold` | Applies semibold font weight. |
| `text-cyan-400` | Applies cyan text color. |
| `mt-3` | Adds top margin. |
| `text-3xl` | Sets the heading font size. |
| `font-bold` | Makes the heading bold. |
| `sm:text-4xl` | Increases heading size at the `sm` breakpoint and above. |
| `mt-8` | Adds space above the skills list. |
| `flex` | Creates a Flexbox layout. |
| `flex-wrap` | Allows skill items to wrap onto new lines. |
| `gap-3` | Adds space between skill items. |
| `rounded-lg` | Gives each skill badge rounded corners. |
| `border` | Adds a border. |
| `border-slate-700` | Applies a slate-colored border. |
| `bg-slate-900` | Adds a dark background. |
| `px-5 py-3` | Adds padding inside each badge. |
| `text-slate-300` | Applies light slate-gray text. |
| `transition` | Animates supported property changes. |
| `hover:border-cyan-400` | Changes the border color on hover. |
| `hover:text-cyan-400` | Changes the text color on hover. |

↓

### What We Learned

- How to create a Skills section.
- How to display skills using the `skills` array.
- How to use the React `map()` method to generate elements dynamically.
- How to use `key={skill}` to identify each rendered item.
- How to create flexible layouts using Flexbox.
- How to make skill badges wrap onto multiple lines.
- How to style badges with borders, padding, and rounded corners.
- How to add hover effects using Tailwind CSS.

</details>

      {/* Projects Section */}


<details>
<summary>06 — Projects Section</summary>

### Code

```tsx
{/* Projects Section */}
<section id="projects" className="bg-slate-900/60">
  <div className="mx-auto max-w-6xl px-6 py-20">
    <p className="font-semibold text-cyan-400">
      WHAT I HAVE BUILT
    </p>

    <h2 className="mt-3 text-3xl font-bold sm:text-4xl">
      Featured Projects
    </h2>

    <div className="mt-10 grid gap-6 md:grid-cols-2 lg:grid-cols-3">
      {projects.map((project) => (
        <article
          key={project.number}
          className="rounded-2xl border border-slate-700 bg-slate-950 p-6 transition duration-300 hover:-translate-y-1 hover:border-cyan-400"
        >
          <p className="text-sm font-semibold text-cyan-400">
            PROJECT {project.number}
          </p>

          <h3 className="mt-4 text-xl font-bold">
            {project.title}
          </h3>

          <p className="mt-3 min-h-20 leading-7 text-slate-400">
            {project.description}
          </p>

          <div className="mt-5 flex flex-wrap gap-2">
            {project.tags.map((tag) => (
              <span
                key={tag}
                className="rounded-md bg-slate-800 px-3 py-1 text-xs text-slate-300"
              >
                {tag}
              </span>
            ))}
          </div>
        </article>
      ))}
    </div>
  </div>
</section>
```

↓

### Tailwind Classes

| Tailwind Class | What It Does |
|---|---|
| `bg-slate-900/60` | Adds a dark background with 60% opacity. |
| `mx-auto` | Centers the container horizontally. |
| `max-w-6xl` | Limits the container width. |
| `px-6 py-20` | Adds horizontal and vertical padding. |
| `font-semibold` | Applies semibold text. |
| `text-cyan-400` | Applies cyan text color. |
| `mt-3` | Adds top margin. |
| `text-3xl` | Sets a large heading size. |
| `font-bold` | Makes text bold. |
| `sm:text-4xl` | Increases heading size on small screens and above. |
| `mt-10` | Adds space above the projects grid. |
| `grid` | Creates a CSS Grid layout. |
| `gap-6` | Adds space between project cards. |
| `md:grid-cols-2` | Displays two columns at the `md` breakpoint and above. |
| `lg:grid-cols-3` | Displays three columns at the `lg` breakpoint and above. |
| `rounded-2xl` | Adds large rounded corners to cards. |
| `border-slate-700` | Applies a slate-colored border. |
| `bg-slate-950` | Adds a very dark background. |
| `p-6` | Adds padding inside each card. |
| `transition` | Animates supported changes. |
| `duration-300` | Sets the transition duration to 300 milliseconds. |
| `hover:-translate-y-1` | Moves the card slightly upward on hover. |
| `hover:border-cyan-400` | Changes the card border to cyan on hover. |
| `text-sm` | Sets small text size. |
| `mt-4` | Adds top margin. |
| `text-xl` | Sets a larger title size. |
| `mt-3` | Adds space above the description. |
| `min-h-20` | Sets a minimum height for the description. |
| `leading-7` | Sets paragraph line height. |
| `mt-5` | Adds space above the tags. |
| `flex flex-wrap` | Arranges tags flexibly and wraps them when needed. |
| `gap-2` | Adds space between tags. |
| `rounded-md` | Adds medium rounded corners. |
| `bg-slate-800` | Applies a dark slate background to tags. |
| `px-3 py-1` | Adds padding inside tags. |
| `text-xs` | Sets extra-small text size. |

↓

### What We Learned

- How to create a Featured Projects section.
- How to display project information from the `projects` array.
- How to use `projects.map()` to render reusable project cards.
- How to display a project number, title, description, and tags.
- How to use `key={project.number}` for React list rendering.
- How to create responsive grids with one, two, or three columns.
- How to style cards using borders, backgrounds, and rounded corners.
- How to create hover animations using `transition` and `hover:-translate-y-1`.
- How to organize project information into reusable data.

</details>

      {/* Contact Section */}


<details>
<summary>07 — Contact Section</summary>

### Code

```tsx
{/* Contact Section */}
<section
  id="contact"
  className="mx-auto max-w-4xl px-6 py-24 text-center"
>
  <p className="font-semibold text-cyan-400">
    LET'S CONNECT
  </p>

  <h2 className="mt-3 text-3xl font-bold sm:text-4xl">
    Have a project in mind?
  </h2>

  <p className="mx-auto mt-5 max-w-xl leading-7 text-slate-400">
    I am always interested in learning, collaborating, and
    exploring new ideas. Feel free to get in touch.
  </p>

  <a
    href="mailto:hsamina590@gmail.com"
    className="mt-8 inline-block rounded-lg bg-cyan-400 px-7 py-3 font-semibold text-slate-950 transition hover:bg-cyan-300"
  >
    Send Me an Email
  </a>
</section>
```

↓

### Tailwind Classes

| Tailwind Class | What It Does |
|---|---|
| `mx-auto` | Centers the section horizontally. |
| `max-w-4xl` | Limits the maximum width of the section. |
| `px-6` | Adds horizontal padding. |
| `py-24` | Adds generous vertical padding. |
| `text-center` | Centers text horizontally. |
| `font-semibold` | Applies semibold font weight. |
| `text-cyan-400` | Applies cyan text color. |
| `mt-3` | Adds top margin. |
| `text-3xl` | Sets heading size. |
| `font-bold` | Makes the heading bold. |
| `sm:text-4xl` | Increases the heading size at the `sm` breakpoint and above. |
| `mt-5` | Adds space above the paragraph. |
| `max-w-xl` | Limits the paragraph width. |
| `leading-7` | Sets line height for readable text. |
| `mt-8` | Adds space above the contact link. |
| `inline-block` | Allows the link to behave like an inline element with block dimensions. |
| `rounded-lg` | Rounds the button corners. |
| `bg-cyan-400` | Adds a cyan background. |
| `px-7 py-3` | Adds padding around the button text. |
| `text-slate-950` | Applies a very dark text color. |
| `transition` | Animates supported style changes. |
| `hover:bg-cyan-300` | Lightens the button background on hover. |

↓

### What We Learned

- How to create a Contact section.
- How to center text and limit content width.
- How to create an email link using `mailto:`.
- How to style a call-to-action link like a button.
- How to add hover effects and smooth transitions.
- How to connect the Contact section to the navbar through `id="contact"`.

</details>

      {/* Footer Section */}


<details>
<summary>08 — Footer Section</summary>

### Code

```tsx
{/* Footer */}
<footer className="border-t border-white/10 px-6 py-6 text-center text-sm text-slate-500">
  © 2026 Samina.dev. Built with Next.js and Tailwind CSS.
</footer>
```

↓

### Tailwind Classes

| Tailwind Class | What It Does |
|---|---|
| `border-t` | Adds a border to the top. |
| `border-white/10` | Applies a white border with 10% opacity. |
| `px-6` | Adds horizontal padding. |
| `py-6` | Adds vertical padding. |
| `text-center` | Centers the footer text. |
| `text-sm` | Sets small text size. |
| `text-slate-500` | Applies muted slate-gray text. |

↓

### What We Learned

- How to create a website footer.
- How to separate the footer using a top border.
- How to center copyright text.
- How to use muted colors for secondary information.
- How to add consistent spacing with padding utilities.
- How to display project technology information in the footer.

</details>

<details>
<summary>09 — Build: Complete Personal Portfolio Website</summary>

### Build Project

Create a complete responsive personal portfolio website using Next.js, React, TypeScript, and Tailwind CSS.

### Required Sections

- Navbar and navigation links
- Hero section with introduction and buttons
- About Me section
- Skills and technologies
- Featured project cards
- Contact section with email link
- Footer with copyright information

### What We Learned

- How to combine multiple sections into one website.
- How to build reusable layouts using React.
- How to display data dynamically using arrays and `map()`.
- How to use Tailwind CSS for responsive design.
- How to style buttons, cards, badges, gradients, and hover effects.
- How to organize a complete personal portfolio project.

</details>


  
## — Build: Complete Personal Portfolio Website

### Build Project

Create a complete responsive personal portfolio website using Next.js, React, TypeScript, and Tailwind CSS.

### Required Sections

* Navbar and navigation links

* Hero section with introduction and buttons

* About Me section

* Skills and technologies

Featured project cards

* Contact section with email link

* Footer with copyright information

### What We Learned

How to combine multiple sections into one website.

How to build reusable layouts using React.

How to display data dynamically using arrays and map().

How to use Tailwind CSS for responsive design.

How to style buttons, cards, badges, gradients, and hover effects.

How to organize a complete personal portfolio project.

