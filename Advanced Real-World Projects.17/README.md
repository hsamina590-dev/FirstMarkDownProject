

const projects = [
  {
    number: "01",
    title: "WeatherNow",
    description:
      "A weather website that displays current weather information using the Open-Meteo API.",
    tags: ["Next.js", "API", "Tailwind CSS"],
  },
  {
    number: "02",
    title: "Westpack",
    description:
      "A web application project for learning registration, login, and user authentication.",
    tags: ["Next.js", "MySQL", "TypeScript"],
  },
  {
    number: "03",
    title: "Tailwind Practice",
    description:
      "A collection of UI exercises for learning layouts, responsive design, and reusable components.",
    tags: ["React", "Tailwind CSS", "GitHub"],
  },
];

const skills = [
  "HTML",
  "CSS",
  "JavaScript",
  "TypeScript",
  "React",
  "Next.js",
  "Tailwind CSS",
  "GitHub",
];

export default function Home() {
  return (
    <main className="min-h-screen bg-slate-950 text-white">
      {/* Navbar */}
      <header className="sticky top-0 z-50 border-b border-white/10 bg-slate-950/95">
        <nav className="mx-auto flex max-w-6xl items-center justify-between px-6 py-5">
          <a href="#home" className="text-2xl font-bold tracking-tight">
            Samina<span className="text-cyan-400">.dev</span>
          </a>

          <div className="flex flex-wrap gap-4 text-sm text-slate-300 sm:gap-7">
            <a href="#about" className="hover:text-cyan-400">About</a>
            <a href="#skills" className="hover:text-cyan-400">Skills</a>
            <a href="#projects" className="hover:text-cyan-400">Projects</a>
            <a href="#contact" className="hover:text-cyan-400">Contact</a>
          </div>
        </nav>
      </header>

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
            <span className="block text-cyan-400">digital experiences.</span>
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

      {/* About Section */}
      <section id="about" className="border-y border-white/10 bg-slate-900/60">
        <div className="mx-auto max-w-6xl px-6 py-20">
          <p className="font-semibold text-cyan-400">GET TO KNOW ME</p>

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

      {/* Projects Section */}
      <section id="projects" className="bg-slate-900/60">
        <div className="mx-auto max-w-6xl px-6 py-20">
          <p className="font-semibold text-cyan-400">WHAT I HAVE BUILT</p>

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

      {/* Contact Section */}
      <section id="contact" className="mx-auto max-w-4xl px-6 py-24 text-center">
        <p className="font-semibold text-cyan-400">LET'S CONNECT</p>

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

      {/* Footer */}
      <footer className="border-t border-white/10 px-6 py-6 text-center text-sm text-slate-500">
        © 2026 Samina.dev. Built with Next.js and Tailwind CSS.
      </footer>
    </main>
  );
}
