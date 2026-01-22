<template>
  <section class="relative py-20 overflow-hidden" id="projects">
    <div class="relative z-10 max-w-8xl mx-auto px-4 sm:6 lg:px-8">
      <div class="text-center mb-16" data-aos="fade-up">
        <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
          My
          <span
            class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400"
          >
            Projects
          </span>
        </h2>
        <p class="text-blue-200 text-lg max-w-2xl mx-auto">
          A Collection Of My Projects, With Both Public And Private Source Code
        </p>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="(project, index) in projects"
          :key="project.id"
          class="group relaive bg-linear-to-br from-gray-600/50 to-blue-900/30 rounded-3xl overflow-hidden border backdrop-blur-sm hover:border-blue-400/30 transition-all duration-500 hover:transform hover:-translate-y-2"
          :class="project.bordColor"
          data-aos="fade-up"
          :data-aos-delay="(index + 1) * 100"
        >
          <div class="relative overflow-hidden">
            <img
              :src="project.image"
              :alt="project.title"
              class="w-full h-48 object-cover group-hover:scale-110 transition-transform duration-500"
            />
            <div
              class="absolute inset-0 bg-linear-to-t from-gray-900 via-transparent to-transparent"
            ></div>
            <div class="absolute top-4 right-4">
              <span
                class="px-3 py-1 text-white text-xs rounded-full font-semibold"
                :class="project.badgeColor"
              >
                {{ project.category }}
              </span>
            </div>
          </div>
          <div class="p-6">
            <h3
              class="text-xl font-bold text-white group-hover:text-blue-400 transition-colors duration-300"
            >
              {{ project.title }}
            </h3>
            <p class="text-blue-100 text-sm leading-relative mb-4">
              {{ project.desc }}
            </p>
            <div class="flex flex-wrap gap-2 mb-4">
              <span
                v-for="tech in project.technolg"
                :key="tech"
                class="px-2 py-1 border rounded text-xs"
                :class="tech.class"
              >
                {{ tech.name }}
              </span>
            </div>
            <div class="flex gap-3">
              <a
                v-for="link in project.links"
                :key="link.name"
                :href="link.url"
                :class="link.class"
                class="flex items-center gap-3 transition-colors duration-300 text-sm font-medium"
              >
                <component :is="link.icon" class="w-4 h-4" />
                {{ link.name }}
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class="text-center mt-16" data-aos="fade-up">
        <div class="inline-flex flex-col sm:flex-row gap-4 items-center">
          <button
            class="px-8 py-4 rounded-xl bg-linear-to-r from-blue-500 to-cyan-500 text-white font-semibold hover:shadow-lg hover:shadow-blue-500/25 transition-all duration-300 hover:scale-105 flex items-center"
          >
            View All Projects
            <ArrowRightIcon class="w-5 h-5 ml-2" />
          </button>
          <button
           @click="scrollToContact"
            class="px-8 py-4 rounded-xl border-2 border-white text-blue-100 font-semibold hover:bg-blue-400/10 transition-all duration-300 flex items-center"
          >
            <ChatBubbleLeftRightIcon class="w-5 h-5 mr-2" />
            Discuss Project
          </button>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import {
  ArrowDownTrayIcon,
  ArrowRightIcon,
  ChatBubbleLeftRightIcon,
  CodeBracketIcon,
  EyeIcon,
} from "@heroicons/vue/16/solid";
import { ref } from "vue";
const scrollToContact = () => {
  const el = document.getElementById("contact")
  if (!el) return

  el.scrollIntoView({ behavior: "smooth" })
}

const projects = ref([
  {
    id: 1,
    title: "Romans Road",
    desc: `A workout regiment web app insipred by Roman legionaries, with a focus on
        bodyweight and weight rucks. Built in Vue.js, and my handcrafted ManuCSS styling 
        for a worn down and aged greek manuscript appearance.`,
    image: "../public/project1.png",
    category: "Frontend",
    bordColor: "border-blue-500/30",
    badgeColor: "bg-blue-500",
    technolg: [
      {
        name: "Vue.js",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
      {
        name: "Tailwind CSS",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
    ],
    links: [
      {
        name: "Website",
        url: "https://romansroad.netlify.app",
        icon: EyeIcon,
        class: "text-white hover:text-blue-300",
      },
    ],
  },
  {
    id: 2,
    title: "C2 - A Discord inspired team communications web app",
    desc: `Full-stack Discord-style web application inspired by military
        communication software like ATAK, built 
        with Next.js 13 and React, featuring real-time 
        messaging via Socket.io, a MySQL database managed with Prisma, and a responsive UI styled with Tailwind CSS.`,
    image: "../public/project2.png",
    category: "Full-stack",
    bordColor: "border-blue-500/30",
    badgeColor: "bg-blue-500",
    technolg: [
      {
        name: "Next.js",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
      {
        name: "React",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
      {
        name: "Socket.io",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
      {
        name: "Clerk",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
      {
        name: "Prisma",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
      {
        name: "Tailwind CSS",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
    ],
    links: [
      {
        name: "Website (Sign-up and Login)",
        url: "#",
        icon: EyeIcon,
        class: "text-white hover:text-blue-300",
      },
      {
        name: "Github Repo",
        url: "#",
        icon: CodeBracketIcon,
        class: "text-white hover:text-blue-300",
      },
    ],
  },

  {
    id: 3,
    title: "Dev Portfolio Template",
    desc: `A Github repository of this very website, built in Vue.js! Supply your own information and images, and customize
    to how you see fit. `,
    image: "../public/project4.png",
    category: "Frontend",
    bordColor: "border-blue-500/30",
    badgeColor: "bg-blue-500",
    technolg: [
      {
        name: "Vue.js",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
      {
        name: "Tailwind CSS",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
    ],
    links: [
      {
        name: "Github Repo",
        url: "#",
        icon: ArrowDownTrayIcon,
        class: "text-white hover:text-blue-300",
      },
    ],
  },
]);
</script>
