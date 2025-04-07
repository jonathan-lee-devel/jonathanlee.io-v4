<script setup lang="ts">
const colorMode = useColorMode()
</script>

<template>
  <div class="min-h-screen bg-gray-100 text-gray-900 dark:bg-gray-900 dark:text-gray-100">
    <!-- Navbar -->
    <header class="w-full bg-white shadow-md dark:bg-gray-800">
      <div class="container mx-auto flex items-center justify-between px-4 py-4 md:px-6">
        <h1 class="text-2xl font-bold tracking-tight">JonathanLee.io</h1>
        <div>
          <Toggle @click="$colorMode.preference = (colorMode.preference === 'light') ? 'dark' : 'light'" >
            <Icon class="text-black dark:text-white" :name="(colorMode.preference === 'light') ? 'lucide:sun' : 'lucide:moon'" size="24" />
          </Toggle>
        </div>
        <nav>
          <ul class="hidden space-x-6 md:flex">
            <li><a href="#about" class="hover:text-blue-500">About</a></li>
            <li><a href="#experience" class="hover:text-blue-500">Experience</a></li>
            <li><a href="#projects" class="hover:text-blue-500">Projects</a></li>
            <li><a href="#contact" class="hover:text-blue-500">Contact</a></li>
          </ul>
          <div class="md:hidden">
            <button id="menu-btn" class="text-blue-500 hover:text-blue-600">
              <!-- Mobile menu icon -->
              <svg
                class="h-6 w-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 8h16M4 16h16"
                ></path>
              </svg>
            </button>
          </div>
        </nav>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="flex items-center justify-center bg-gray-100 py-20 dark:bg-gray-900">
      <div class="space-y-6 px-8 text-center">
        <h2 class="text-4xl font-extrabold leading-tight md:text-6xl">
          Hi, I’m <span class="text-blue-500">Jonathan Lee</span>
        </h2>
        <p class="text-lg text-gray-700 dark:text-gray-300 md:text-xl">
          A passionate Software Engineer blending creativity and technology to build impactful
          solutions. I love working on open-source and closed-source personal projects to continually enhance my skills.
        </p>
        <div class="space-y-4 sm:space-x-4 sm:space-y-0 grid grid-cols-1 sm:grid-cols-3">
          <a
            href="#projects"
            class="rounded-lg bg-blue-500 px-6 py-3 text-center text-white hover:bg-blue-600"
          >
            View My Work
          </a>
          <a
            href="#contact"
            class="rounded-lg border border-gray-300 px-6 py-3 text-center hover:bg-gray-200 dark:border-gray-700 dark:hover:bg-gray-800"
          >
            Contact Me
          </a>
          <!-- Download Resume/CV Button -->
          <a
            href="/Jonathan_Lee_CV_2025.pdf"
            download
            class="rounded-lg bg-blue-500 px-6 py-3 text-center text-white hover:bg-blue-600"
          >
            Download CV/Resume
          </a>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section
      id="about"
      class="border-t border-gray-200 bg-white py-20 dark:border-gray-700 dark:bg-gray-800"
    >
      <div class="container mx-auto max-w-4xl space-y-6 px-6">
        <h3 class="text-3xl font-semibold">About Me</h3>
        <p class="text-gray-700 dark:text-gray-300">
          Passionate and experienced software engineer with developed teamwork, communication, and problem-solving skills.
          A reliable and punctilious individual with a strong work ethic.
          Proven capability of working and learning on my own initiative, very adaptable, and happy to work as part of a team as demonstrated by career progression from Undergraduate to Graduate to Software Engineer II while working for major international brands of 30,000-100,000+ employees and annual revenue in the range of $20B+.
        </p>
        <p class="text-gray-700 dark:text-gray-300">
          Whether working on frontend designs or backend challenges, I aim to make a difference by
          using technology to solve problems, simplify workflows, and create enjoyable user
          experiences.
        </p>
      </div>
    </section>

    <!-- Work Experience Section -->
    <section
      id="experience"
      class="border-t border-gray-200 bg-gray-100 py-20 dark:border-gray-700 dark:bg-gray-900"
    >
      <div class="container mx-auto max-w-5xl space-y-10 px-4 sm:px-6 lg:px-8">
        <h3 class="text-center text-3xl font-semibold">Work Experience</h3>
        <div class="space-y-8">
          <!-- Job 1 -->
          <div class="rounded-lg bg-white p-6 shadow-md dark:bg-gray-800">
            <div class="flex flex-col items-start justify-between sm:flex-row sm:items-center">
              <h4 class="text-xl font-semibold">Software Engineer @ Fidelity Investments</h4>
              <span class="mt-2 text-gray-500 dark:text-gray-400 sm:mt-0">Nov 2023 - Present</span>
            </div>
            <p class="mt-4 text-gray-700 dark:text-gray-300">
              Operated within an Agile development process on Fidelity’s internal global intranet, serving all 80,000+ employees across the globe.
              The application is built using a modern microservices architecture composed of 25 individual microservices.
              The site acts as a global employee directory, source of informational news articles and company events, and more recently an internal search engine powered by ElasticSearch.
            </p>

            <!-- Responsive Tags -->
            <div class="mt-4 flex flex-wrap gap-2">
              <span class="rounded-lg bg-green-100 px-3 py-1 text-sm font-medium text-green-600"
                >Full-stack</span
              >
              <span class="rounded-lg bg-blue-100 px-3 py-1 text-sm font-medium text-blue-600"
                >Kubernetes</span
              >
              <span class="rounded-lg bg-red-200 px-3 py-1 text-sm font-medium text-red-600"
                >Cloud / AWS</span
              >
              <span class="rounded-lg bg-gray-200 px-3 py-1 text-sm font-medium text-gray-600"
                >Microservices</span
              >
              <span class="rounded-lg bg-cyan-200 px-3 py-1 text-sm font-medium text-cyan-600"
                >Java</span
              >
              <span class="rounded-lg bg-pink-200 px-3 py-1 text-sm font-medium text-pink-600"
                >Angular</span
              >
            </div>

            <ul class="mt-4 list-inside list-disc text-gray-700 dark:text-gray-300">
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
          <div class="rounded-lg bg-white p-6 shadow-md dark:bg-gray-800">
            <div class="flex flex-col items-start justify-between sm:flex-row sm:items-center">
              <h4 class="text-xl font-semibold">Software Engineer II @ MasterCard</h4>
              <span class="mt-2 text-gray-500 dark:text-gray-400 sm:mt-0">Jan 2023 - Nov 2023</span>
            </div>
            <p class="mt-4 text-gray-700 dark:text-gray-300">
              Worked in an Agile development process on MasterCard’s business-to-business Smart Data solution.
              A large Spring Boot application deployed using Apache Tomcat. Serving millions of monthly active customers globally.
              Successfully implemented various pieces of functionality which underwent stringent testing from QA Engineers.
              Managed the release of artifacts to live environments including Production.
            </p>

            <!-- Responsive Tags -->
            <div class="mt-4 flex flex-wrap gap-2">
              <span class="rounded-lg bg-green-100 px-3 py-1 text-sm font-medium text-green-600"
                >Backend</span
              >
              <span class="rounded-lg bg-red-200 px-3 py-1 text-sm font-medium text-red-600"
                >B2B / Finance</span
              >
              <span class="rounded-lg bg-cyan-200 px-3 py-1 text-sm font-medium text-cyan-600"
                >Java</span
              >
            </div>

            <ul class="mt-4 list-inside list-disc text-gray-700 dark:text-gray-300">
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
          <div class="rounded-lg bg-white p-6 shadow-md dark:bg-gray-800">
            <div class="flex flex-col items-start justify-between sm:flex-row sm:items-center">
              <h4 class="text-xl font-semibold">Software Engineer @ Ericsson</h4>
              <span class="mt-2 text-gray-500 dark:text-gray-400 sm:mt-0">Nov 2021 - Jan 2023</span>
            </div>
            <p class="mt-4 text-gray-700 dark:text-gray-300">
              Implemented various pieces of functionality in a resource pooling tool developed as a fully-featured web application using the MEAN stack, as well as a command-line interface developed in Python.
              Worked alongside various other teams to build a software platform with a strong emphasis on reliability, reusability, and scalability.
            </p>

            <!-- Responsive Tags -->
            <div class="mt-4 flex flex-wrap gap-2">
              <span class="rounded-lg bg-green-100 px-3 py-1 text-sm font-medium text-green-600"
                >Full-stack</span
              >
              <span class="rounded-lg bg-blue-100 px-3 py-1 text-sm font-medium text-blue-600"
                >Kubernetes</span
              >
              <span class="rounded-lg bg-red-200 px-3 py-1 text-sm font-medium text-red-600"
                >Node.js</span
              >
              <span class="rounded-lg bg-yellow-200 px-3 py-1 text-sm font-medium text-yellow-600"
                >Python</span
              >
              <span class="rounded-lg bg-cyan-200 px-3 py-1 text-sm font-medium text-cyan-600"
                >JavaScript</span
              >
              <span class="rounded-lg bg-pink-200 px-3 py-1 text-sm font-medium text-pink-600"
                >Angular</span
              >
            </div>

            <ul class="mt-4 list-inside list-disc text-gray-700 dark:text-gray-300">
              <li>
                Introduced end-to-end testing using Cypress to ensure quality and reliability.
              </li>
              <li>
                Refined internal dashboard using Angular Material and dynamic data visualization.
              </li>
              <li>
                Implemented new feature using MongoDB features such as Aggregation Pipelines, and enhanced queries.
              </li>
            </ul>
          </div>

          <!-- Job 4 -->
          <div class="rounded-lg bg-white p-6 shadow-md dark:bg-gray-800">
            <div class="flex flex-col items-start justify-between sm:flex-row sm:items-center">
              <h4 class="text-xl font-semibold">Undergraduate Software Developer @ Jaguar Land Rover</h4>
              <span class="mt-2 text-gray-500 dark:text-gray-400 sm:mt-0">Jan 2020 - Sep 2020</span>
            </div>
            <p class="mt-4 text-gray-700 dark:text-gray-300">
              Worked alongside teams based in Ireland and England to build a software platform with a strong emphasis on reliability, reusability, and scalability.
              Worked on a B2B Spring Boot project deployed to a Kubernetes cluster on Google Cloud Platform.
            </p>

            <!-- Responsive Tags -->
            <div class="mt-4 flex flex-wrap gap-2">
              <span class="rounded-lg bg-green-100 px-3 py-1 text-sm font-medium text-green-600"
              >Backend</span
              >
              <span class="rounded-lg bg-blue-100 px-3 py-1 text-sm font-medium text-blue-600"
              >Kubernetes</span
              >
              <span class="rounded-lg bg-red-200 px-3 py-1 text-sm font-medium text-red-600"
              >Java</span
              >
              <span class="rounded-lg bg-yellow-200 px-3 py-1 text-sm font-medium text-yellow-600"
              >Python</span
              >
              <span class="rounded-lg bg-cyan-200 px-3 py-1 text-sm font-medium text-cyan-600"
              >JavaScript</span
              >
            </div>

            <ul class="mt-4 list-inside list-disc text-gray-700 dark:text-gray-300">
              <li>
                Implemented various components of the software platform including Controllers, Services, and Repositories.
              </li>
              <li>
                Created a helper script to automate the generation of REST API documentation for the 200+ endpoints.
              </li>
              <li>
                Worked on a separate in-house solution deployed to a vehicles on-board computer for learning purposes.
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="bg-gray-100 py-20 dark:bg-gray-900">
      <div class="container mx-auto space-y-6 px-6">
        <h3 class="text-center text-3xl font-semibold">Personal Projects</h3>
        <div class="mt-10 grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
          <!-- Project Card -->
          <div
            class="transform rounded-lg bg-white p-6 shadow-lg transition hover:-translate-y-2 dark:bg-gray-800"
          >
            <h4 class="text-xl font-semibold">www.RoomyLedger.com</h4>
            <p class="mt-2 text-gray-700 dark:text-gray-300">
              A personal finance application for people living in shared accommodation.
            </p>

            <!-- Tags -->
            <div class="mt-4 flex flex-wrap space-x-2">
              <span class="rounded-lg bg-green-100 px-3 py-1 text-sm font-medium text-green-600"
                >Node.js</span
              >
              <span class="rounded-lg bg-red-100 px-3 py-1 text-sm font-medium text-red-600"
                >NestJS</span
              >
              <span class="rounded-lg bg-pink-200 px-3 py-1 text-sm font-medium text-pink-600"
                >Angular</span
              >
            </div>

            <!-- Learn More -->
            <a
              href="https://www.roomyledger.com"
              target="_blank"
              class="mt-4 block text-blue-500 transition hover:underline"
            >
              Visit Site
            </a>

            <!-- GitHub Button -->
            <h3 class="pt-4 mt-4">This project is open-source, why not</h3>
            <a
              href="https://github.com/jonathan-lee-devel/roomyledger"
              target="_blank"
              rel="noopener noreferrer"
              class="mt-6 inline-block rounded-lg bg-blue-500 px-4 py-2 text-white transition hover:bg-blue-600"
            >
              ⭐ Give it a Star
            </a>
          </div>

          <!-- Repeat Project Cards -->
          <div
            class="transform rounded-lg bg-white p-6 shadow-lg transition hover:-translate-y-2 dark:bg-gray-800"
          >
            <h4 class="text-xl font-semibold">www.EchoNexus.io</h4>
            <p class="mt-2 text-gray-700 dark:text-gray-300">
              An all-in-one feedback platform for your own website. Embeddable feedback widget that works with any website.
            </p>

            <!-- Tags -->
            <div class="mt-4 flex flex-wrap space-x-2">
              <span class="rounded-lg bg-green-100 px-3 py-1 text-sm font-medium text-green-600"
                >Node.js</span
              >
              <span class="rounded-lg bg-red-100 px-3 py-1 text-sm font-medium text-red-600"
                >NestJS</span
              >
              <span class="rounded-lg bg-pink-200 px-3 py-1 text-sm font-medium text-pink-600"
                >Angular</span
              >
            </div>

            <!-- Learn More -->
            <a
              href="https://www.echonexus.io"
              target="_blank"
              class="mt-4 block text-blue-500 transition hover:underline"
            >
              Visit Site
            </a>

            <h3 class="pt-4 mt-4">This project is closed-source, hence, no GitHub link</h3>
          </div>

          <div
            class="transform rounded-lg bg-white p-6 shadow-lg transition hover:-translate-y-2 dark:bg-gray-800"
          >
            <h4 class="text-xl font-semibold">Jenkify</h4>
            <p class="mt-2 text-gray-700 dark:text-gray-300">
              A dockerized CLI tool for orchestrating Jenkins pipelines.
            </p>

            <!-- Tags -->
            <div class="mt-4 flex flex-wrap space-x-2">
              <span class="rounded-lg bg-green-100 px-3 py-1 text-sm font-medium text-green-600"
                >Node.js</span
              >
              <span class="rounded-lg bg-red-100 px-3 py-1 text-sm font-medium text-red-600"
                >NestJS</span
              >
              <span class="rounded-lg bg-gray-200 px-3 py-1 text-sm font-medium text-gray-600"
                >CLI</span
              >
            </div>

            <!-- GitHub Button -->
            <h3 class="pt-4 mt-4">This project is open-source, why not</h3>
            <a
              href="https://github.com/jonathan-lee-devel/jenkify-v2"
              target="_blank"
              rel="noopener noreferrer"
              class="mt-6 inline-block rounded-lg bg-blue-500 px-4 py-2 text-white transition hover:bg-blue-600"
            >
              ⭐ Give it a Star
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="bg-white py-20 dark:bg-gray-800">
      <div class="container mx-auto max-w-3xl space-y-4 px-6 text-center">
        <h3 class="text-3xl font-semibold">Get in Touch</h3>
        <p class="text-gray-700 dark:text-gray-300">
          I’m always excited to connect! Feel free to reach out to discuss projects, opportunities,
          or just to have a chat.
        </p>
        <div class="mt-6 flex justify-center space-x-6">
          <a
            href="https://linkedin.com/in/jonathan-lee-devel"
            target="_blank"
            rel="noopener noreferrer"
            class="flex items-center space-x-2 text-blue-500 hover:text-blue-600"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.761 0 5-2.239 5-5v-14c0-2.761-2.239-5-5-5zm-11 19h-3v-10h3v10zm-1.5-11.5c-.828 0-1.5-.672-1.5-1.5s.672-1.5 1.5-1.5 1.5.672 1.5 1.5-.672 1.5-1.5 1.5zm13.5 11.5h-3v-5.5c0-1.381-1.119-2.5-2.5-2.5s-2.5 1.119-2.5 2.5v5.5h-3v-10h3v1.5c.41-.771 1.649-1.5 2.5-1.5 2.485 0 3.5 2.015 3.5 4.5v5.5z"
              />
            </svg>
            <span>LinkedIn</span>
          </a>
          <a
            href="https://github.com/jonathan-lee-devel"
            target="_blank"
            rel="noopener noreferrer"
            class="flex items-center space-x-2 text-blue-500 hover:text-blue-600"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.385.6.113.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.757-1.333-1.757-1.089-.744.084-.729.084-.729 1.205.085 1.839 1.237 1.839 1.237 1.07 1.834 2.809 1.304 3.495.997.108-.775.419-1.305.762-1.605-2.665-.305-5.466-1.334-5.466-5.931 0-1.312.469-2.382 1.236-3.221-.124-.305-.535-1.527.117-3.178 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.398 3.003-.403 1.02.005 2.047.137 3.005.403 2.29-1.553 3.296-1.23 3.296-1.23.653 1.651.242 2.873.118 3.178.77.839 1.236 1.909 1.236 3.221 0 4.609-2.805 5.624-5.475 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.577 4.765-1.588 8.198-6.084 8.198-11.384 0-6.627-5.373-12-12-12z"
              />
            </svg>
            <span>GitHub</span>
          </a>
        </div>
      </div>
    </section>
  </div>
</template>
