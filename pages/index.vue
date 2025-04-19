<script setup lang="ts">
const colorMode = useColorMode()

function toggleColorMode() {
  colorMode.preference = colorMode.value === 'light' ? 'dark' : 'light'
}
</script>

<template>
  <div class="min-h-screen bg-gray-50 text-gray-900 transition-colors duration-300 dark:bg-gray-950 dark:text-gray-100">
    <!-- Navbar -->
    <header class="sticky top-0 z-50 w-full border-b border-gray-200/80 bg-white/80 shadow-sm backdrop-blur-sm transition-colors duration-300 dark:border-gray-700/80 dark:bg-gray-900/80">
      <div class="container mx-auto flex h-16 items-center justify-between px-4 md:px-6">
        <a href="/" class="text-2xl font-bold tracking-tight hover:text-blue-600 dark:hover:text-blue-400">JonathanLee.io</a>
        <nav class="flex items-center space-x-6">
          <ul class="hidden space-x-6 md:flex">
            <li><a href="#about" class="text-sm font-medium text-gray-600 transition-colors hover:text-blue-500 dark:text-gray-400 dark:hover:text-blue-400">About</a></li>
            <li><a href="#experience" class="text-sm font-medium text-gray-600 transition-colors hover:text-blue-500 dark:text-gray-400 dark:hover:text-blue-400">Experience</a></li>
            <li><a href="#projects" class="text-sm font-medium text-gray-600 transition-colors hover:text-blue-500 dark:text-gray-400 dark:hover:text-blue-400">Projects</a></li>
            <li><a href="#contact" class="text-sm font-medium text-gray-600 transition-colors hover:text-blue-500 dark:text-gray-400 dark:hover:text-blue-400">Contact</a></li>
          </ul>
           <!-- Color Mode Toggle -->
          <button
            @click="toggleColorMode"
            class="flex h-9 w-9 items-center justify-center rounded-full border border-gray-300 text-gray-700 transition-colors hover:bg-gray-100 dark:border-gray-700 dark:text-gray-300 dark:hover:bg-gray-800"
            aria-label="Toggle color mode"
          >
            <Icon class="text-black dark:text-white" :name="(colorMode.value === 'light') ? 'lucide:sun' : 'lucide:moon'" size="18" />
          </button>
          <div class="md:hidden">
             <!-- Mobile menu button - functionality needs implementation -->
            <button id="menu-btn" class="rounded p-1.5 text-gray-600 hover:bg-gray-100 dark:text-gray-400 dark:hover:bg-gray-800">
              <svg
                class="h-6 w-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="2"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M4 6h16M4 12h16m-7 6h7"
                />
              </svg>
              <span class="sr-only">Open menu</span>
            </button>
          </div>
        </nav>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="flex items-center justify-center bg-gray-50 py-24 sm:py-32 dark:bg-gray-950">
      <div class="max-w-3xl space-y-8 px-6 text-center lg:px-8">
        <h2 class="text-4xl font-extrabold tracking-tight sm:text-5xl md:text-6xl">
          Hi, I’m <span class="text-blue-600 dark:text-blue-400">Jonathan Lee</span>
        </h2>
        <p class="text-lg leading-relaxed text-gray-600 dark:text-gray-300 md:text-xl">
          A passionate Software Engineer blending creativity and technology to build impactful
          solutions. I love working on open-source and closed-source personal projects to continually enhance my skills.
        </p>
        <div class="flex flex-col items-center justify-center gap-4 sm:flex-row sm:gap-6">
          <a
            href="#projects"
            class="inline-flex h-11 items-center justify-center rounded-md bg-blue-600 px-6 text-sm font-medium text-white shadow-sm transition-colors hover:bg-blue-700 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600 dark:bg-blue-500 dark:hover:bg-blue-600 dark:focus-visible:outline-blue-500"
          >
            View My Work
          </a>
          <a
            href="#contact"
            class="inline-flex h-11 items-center justify-center rounded-md border border-gray-300 bg-white px-6 text-sm font-medium text-gray-700 shadow-sm transition-colors hover:bg-gray-100 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600 dark:border-gray-700 dark:bg-gray-800 dark:text-gray-300 dark:hover:bg-gray-700"
          >
            Contact Me
          </a>
          <a
            href="/Jonathan_Lee_CV_2025.pdf"
            download
            class="inline-flex h-11 items-center justify-center rounded-md bg-gray-700 px-6 text-sm font-medium text-white shadow-sm transition-colors hover:bg-gray-800 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-gray-700 dark:bg-gray-600 dark:hover:bg-gray-500 dark:focus-visible:outline-gray-600"
          >
            Download CV/Resume
          </a>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section
      id="about"
      class="border-t border-gray-200 bg-white py-24 dark:border-gray-800 dark:bg-gray-900 sm:py-32"
    >
      <div class="container mx-auto max-w-4xl space-y-6 px-6 lg:px-8">
        <h3 class="text-3xl font-semibold tracking-tight sm:text-4xl">About Me</h3>
        <div class="space-y-4 text-lg leading-relaxed text-gray-700 dark:text-gray-300">
             <p>
               Passionate and experienced software engineer with developed teamwork, communication, and problem-solving skills.
               A reliable and punctilious individual with a strong work ethic.
               Proven capability of working and learning on my own initiative, very adaptable, and happy to work as part of a team as demonstrated by career progression from Undergraduate to Graduate to Software Engineer II while working for major international brands of 30,000-100,000+ employees and annual revenue in the range of $20B+.
             </p>
             <p>
               Whether working on frontend designs or backend challenges, I aim to make a difference by
               using technology to solve problems, simplify workflows, and create enjoyable user
               experiences.
             </p>
        </div>
      </div>
    </section>

    <!-- Work Experience Section -->
    <section
      id="experience"
      class="border-t border-gray-200 bg-gray-50 py-24 dark:border-gray-800 dark:bg-gray-950 sm:py-32"
    >
      <div class="container mx-auto max-w-5xl space-y-12 px-4 sm:px-6 lg:px-8">
        <h3 class="text-center text-3xl font-semibold tracking-tight sm:text-4xl">Work Experience</h3>
        <div class="space-y-10">
          <!-- Job 1 -->
          <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm transition-shadow duration-200 hover:shadow-md dark:border-gray-700 dark:bg-gray-900 dark:hover:shadow-lg dark:hover:shadow-blue-500/10 sm:p-8">
            <div class="flex flex-col items-start justify-between gap-2 sm:flex-row sm:items-center">
              <h4 class="text-xl font-semibold">Software Engineer @ Fidelity Investments</h4>
              <span class="text-sm text-gray-500 dark:text-gray-400">Nov 2023 - Present</span>
            </div>
            <p class="mt-4 text-gray-700 dark:text-gray-300">
              Operated within an Agile development process on Fidelity’s internal global intranet, serving all 80,000+ employees across the globe.
              The application is built using a modern microservices architecture composed of 25 individual microservices.
              The site acts as a global employee directory, source of informational news articles and company events, and more recently an internal search engine powered by ElasticSearch.
            </p>

            <!-- Responsive Tags -->
            <div class="mt-5 flex flex-wrap gap-2">
              <span class="inline-flex items-center rounded-md bg-green-50 px-2.5 py-0.5 text-sm font-medium text-green-700 ring-1 ring-inset ring-green-600/20 dark:bg-green-500/10 dark:text-green-400 dark:ring-green-500/20">Full-stack</span>
              <span class="inline-flex items-center rounded-md bg-blue-50 px-2.5 py-0.5 text-sm font-medium text-blue-700 ring-1 ring-inset ring-blue-600/20 dark:bg-blue-500/10 dark:text-blue-400 dark:ring-blue-500/20">Kubernetes</span>
              <span class="inline-flex items-center rounded-md bg-red-50 px-2.5 py-0.5 text-sm font-medium text-red-700 ring-1 ring-inset ring-red-600/20 dark:bg-red-500/10 dark:text-red-400 dark:ring-red-500/20">Cloud / AWS</span>
              <span class="inline-flex items-center rounded-md bg-gray-100 px-2.5 py-0.5 text-sm font-medium text-gray-700 ring-1 ring-inset ring-gray-600/20 dark:bg-gray-500/10 dark:text-gray-400 dark:ring-gray-500/20">Microservices</span>
              <span class="inline-flex items-center rounded-md bg-cyan-50 px-2.5 py-0.5 text-sm font-medium text-cyan-700 ring-1 ring-inset ring-cyan-600/20 dark:bg-cyan-500/10 dark:text-cyan-400 dark:ring-cyan-500/20">Java</span>
              <span class="inline-flex items-center rounded-md bg-pink-50 px-2.5 py-0.5 text-sm font-medium text-pink-700 ring-1 ring-inset ring-pink-600/20 dark:bg-pink-500/10 dark:text-pink-400 dark:ring-pink-500/20">Angular</span>
            </div>

            <ul class="mt-5 space-y-1 list-inside list-disc text-gray-700 dark:text-gray-300">
              <li>
                Developed and deployed scalable web applications using Spring Boot and Java.
              </li>
              <li>
                Followed strict guidelines to ensure code quality and minimal downtime.
              </li>
              <li>
                Performed various upgrades of Spring Boot versions and Angular versions, key to ensuring security and stability.
              </li>
            </ul>
          </div>

          <!-- Job 2 -->
          <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm transition-shadow duration-200 hover:shadow-md dark:border-gray-700 dark:bg-gray-900 dark:hover:shadow-lg dark:hover:shadow-blue-500/10 sm:p-8">
            <div class="flex flex-col items-start justify-between gap-2 sm:flex-row sm:items-center">
              <h4 class="text-xl font-semibold">Software Engineer II @ MasterCard</h4>
              <span class="text-sm text-gray-500 dark:text-gray-400">Jan 2023 - Nov 2023</span>
            </div>
            <p class="mt-4 text-gray-700 dark:text-gray-300">
              Worked in an Agile development process on MasterCard’s business-to-business Smart Data solution.
              A large Spring Boot application deployed using Apache Tomcat. Serving millions of monthly active customers globally.
              Successfully implemented various pieces of functionality which underwent stringent testing from QA Engineers.
              Managed the release of artifacts to live environments including Production.
            </p>

            <!-- Responsive Tags -->
            <div class="mt-5 flex flex-wrap gap-2">
               <span class="inline-flex items-center rounded-md bg-green-50 px-2.5 py-0.5 text-sm font-medium text-green-700 ring-1 ring-inset ring-green-600/20 dark:bg-green-500/10 dark:text-green-400 dark:ring-green-500/20">Backend</span>
               <span class="inline-flex items-center rounded-md bg-red-50 px-2.5 py-0.5 text-sm font-medium text-red-700 ring-1 ring-inset ring-red-600/20 dark:bg-red-500/10 dark:text-red-400 dark:ring-red-500/20">B2B / Finance</span>
               <span class="inline-flex items-center rounded-md bg-cyan-50 px-2.5 py-0.5 text-sm font-medium text-cyan-700 ring-1 ring-inset ring-cyan-600/20 dark:bg-cyan-500/10 dark:text-cyan-400 dark:ring-cyan-500/20">Java</span>
            </div>

            <ul class="mt-5 space-y-1 list-inside list-disc text-gray-700 dark:text-gray-300">
              <li>
                Refactored legacy code to ensure code quality and minimal downtime.
              </li>
              <li>
                Kept software up-to-date with latest secure clients for inter-company communication.
              </li>
              <li>
                Participated in large release efforts, ensuring smooth and timely delivery of new features.
              </li>
            </ul>
          </div>

          <!-- Job 3 -->
          <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm transition-shadow duration-200 hover:shadow-md dark:border-gray-700 dark:bg-gray-900 dark:hover:shadow-lg dark:hover:shadow-blue-500/10 sm:p-8">
            <div class="flex flex-col items-start justify-between gap-2 sm:flex-row sm:items-center">
              <h4 class="text-xl font-semibold">Software Engineer @ Ericsson</h4>
               <span class="text-sm text-gray-500 dark:text-gray-400">Nov 2021 - Jan 2023</span>
            </div>
            <p class="mt-4 text-gray-700 dark:text-gray-300">
              Implemented various pieces of functionality in a resource pooling tool developed as a fully-featured web application using the MEAN stack, as well as a command-line interface developed in Python.
              Worked alongside various other teams to build a software plat... <!-- Truncated -->
            </p>
            <!-- Responsive Tags -->
            <div class="mt-5 flex flex-wrap gap-2">
              <span class="inline-flex items-center rounded-md bg-green-50 px-2.5 py-0.5 text-sm font-medium text-green-700 ring-1 ring-inset ring-green-600/20 dark:bg-green-500/10 dark:text-green-400 dark:ring-green-500/20">Full-stack</span>
              <span class="inline-flex items-center rounded-md bg-blue-50 px-2.5 py-0.5 text-sm font-medium text-blue-700 ring-1 ring-inset ring-blue-600/20 dark:bg-blue-500/10 dark:text-blue-400 dark:ring-blue-500/20">Kubernetes</span>
              <span class="inline-flex items-center rounded-md bg-red-50 px-2.5 py-0.5 text-sm font-medium text-red-700 ring-1 ring-inset ring-red-600/20 dark:bg-red-500/10 dark:text-red-400 dark:ring-red-500/20">Cloud / AWS</span>
              <span class="inline-flex items-center rounded-md bg-gray-100 px-2.5 py-0.5 text-sm font-medium text-gray-700 ring-1 ring-inset ring-gray-600/20 dark:bg-gray-500/10 dark:text-gray-400 dark:ring-gray-500/20">Microservices</span>
              <span class="inline-flex items-center rounded-md bg-cyan-50 px-2.5 py-0.5 text-sm font-medium text-cyan-700 ring-1 ring-inset ring-cyan-600/20 dark:bg-cyan-500/10 dark:text-cyan-400 dark:ring-cyan-500/20">Node.js</span>
              <span class="inline-flex items-center rounded-md bg-pink-50 px-2.5 py-0.5 text-sm font-medium text-pink-700 ring-1 ring-inset ring-pink-600/20 dark:bg-pink-500/10 dark:text-pink-400 dark:ring-pink-500/20">Angular</span>
            </div>

            <ul class="mt-5 space-y-1 list-inside list-disc text-gray-700 dark:text-gray-300">
              <li>
                Developed and deployed scalable web applications using Spring Boot and Java.
              </li>
              <li>
                Followed strict guidelines to ensure code quality and minimal downtime.
              </li>
              <li>
                Performed various upgrades of Spring Boot versions and Angular versions, key to ensuring security and stability.
              </li>
            </ul>
          </div>
        </div>

        <div class="rounded-lg border border-gray-200 bg-white p-6 shadow-sm transition-shadow duration-200 hover:shadow-md dark:border-gray-700 dark:bg-gray-900 dark:hover:shadow-lg dark:hover:shadow-blue-500/10 sm:p-8">
          <div class="flex flex-col items-start justify-between gap-2 sm:flex-row sm:items-center">
            <h4 class="text-xl font-semibold">Undergraduate Software Developer @ Jaguar Land Rover</h4>
            <span class="text-sm text-gray-500 dark:text-gray-400">Jan 2020 - Sep 2020</span>
          </div>
          <p class="mt-4 text-gray-700 dark:text-gray-300">
            Worked in an Agile development process on a brand new B2B data platform for their next generation of vehicle data APIs and technology.
          </p>

          <!-- Responsive Tags -->
          <div class="mt-5 flex flex-wrap gap-2">
            <span class="inline-flex items-center rounded-md bg-green-50 px-2.5 py-0.5 text-sm font-medium text-green-700 ring-1 ring-inset ring-green-600/20 dark:bg-green-500/10 dark:text-green-400 dark:ring-green-500/20">Backend</span>
            <span class="inline-flex items-center rounded-md bg-blue-50 px-2.5 py-0.5 text-sm font-medium text-blue-700 ring-1 ring-inset ring-blue-600/20 dark:bg-blue-500/10 dark:text-blue-400 dark:ring-blue-500/20">Kubernetes</span>
            <span class="inline-flex items-center rounded-md bg-red-50 px-2.5 py-0.5 text-sm font-medium text-blue-950 ring-1 ring-inset ring-red-600/20 dark:bg-red-500/10 dark:text-red-400 dark:ring-red-500/20">Cloud / GCP</span>
            <span class="inline-flex items-center rounded-md bg-cyan-50 px-2.5 py-0.5 text-sm font-medium text-cyan-700 ring-1 ring-inset ring-cyan-600/20 dark:bg-cyan-500/10 dark:text-cyan-400 dark:ring-cyan-500/20">Java</span>
            <span class="inline-flex items-center rounded-md bg-red-50 px-2.5 py-0.5 text-sm font-medium text-red-700 ring-1 ring-inset ring-red-600/20 dark:bg-red-500/10 dark:text-red-400 dark:ring-red-500/20">B2B</span>
          </div>

          <ul class="mt-5 space-y-1 list-inside list-disc text-gray-700 dark:text-gray-300">
            <li>
              Investigated frameworks and libraries for use with the greenfield project.
            </li>
            <li>
              Implemented helper script to auto-generate OpenAPI documentation for 200+ endpoints.
            </li>
            <li>
              Delivered an initial minimum-viable product (MVP) in the space of 6 months.
            </li>
          </ul>
        </div>
      </div>
    </section>

    <!-- Other sections (Projects, Contact, Footer) would follow similar patterns -->

  </div>
</template>