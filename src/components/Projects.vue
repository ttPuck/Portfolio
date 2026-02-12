<template>
  <section class="relative py-20 overflow-hidden" id="projects">
    <div class="relative z-10 max-w-8xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16" data-aos="fade-up">
        <h2 class="text-4xl md:text-5xl font-bold text-(--color-text) mb-4">
          My
          <span
            class="text-transparent bg-clip-text bg-linear-to-r from-[#b14aed] to-[#454ade]"
          >
            Web Development Projects
          </span>
        </h2>
        <p class="text-(--color-text) text-lg max-w-2xl mx-auto">
          A Collection Of My Web Development Projects
        </p>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-3 gap-8">
        <div
          v-for="(webproject, index) in webprojects"
          :key="webproject.id"
          class="group relative bg-(--color-primaryalt) rounded-3xl overflow-hidden border backdrop-blur-sm hover:border-[#a73ee4] transition-all duration-500 hover:transform hover:-translate-y-2"
          :class="webproject.bordColor"
          data-aos="fade-up"
          :data-aos-delay="(index + 1) * 100"
        >
          <div class="relative overflow-hidden">
            <img
              :src="webproject.image"
              :alt="webproject.title"
              class="w-full h-48 object-cover group-hover:scale-110 transition-transform duration-500"
            />
            <div
              class="absolute inset-0 bg-linear-to-t from-gray-900 via-transparent to-transparent"
            ></div>
            <div class="absolute top-4 right-4">
              <span
                class="px-3 py-1 text-white text-xs rounded-full font-semibold"
                :class="webproject.badgeColor"
              >
                {{ webproject.category }}
              </span>
            </div>
          </div>
          <div class="p-6">
            <h3
              class="text-xl font-bold text-white group-hover:text-(--color-sidealt) transition-colors duration-300"
            >
              {{ webproject.title }}
            </h3>
            <p class="text-blue-100 text-sm leading-relaxed mb-4">
              {{ webproject.desc }}
            </p>
            <div class="flex flex-wrap gap-2 mb-4">
              <span
                v-for="tech in webproject.technolg"
                :key="tech"
                class="px-2 py-1 border rounded text-xs"
                :class="tech.class"
              >
                {{ tech.name }}
              </span>
            </div>
            <div class="flex gap-3">
              <a
                v-for="link in webproject.links"
                :key="link.name"
                :href="link.url"
                target="_blank"
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
      <div class="text-center mt-16" data-aos="fade-up"></div>
    </div>
  </section>
  <!-- BREAKER -->
  <section class="relative py-20 overflow-hidden" id="projects">
    <div class="relative z-10 max-w-8xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16" data-aos="fade-up">
        <h2 class="text-4xl md:text-5xl font-bold text-(--color-text) mb-4">
          My
          <span
            class="text-transparent text bg-clip-text bg-linear-to-r from-[#b14aed] to-[#454ade]"
          >
            Other Projects
          </span>
        </h2>
        <p class="text-(--color-text) text-lg max-w-2xl mx-auto">
          A Collection Of My App & Game Projects, All Open Source!
        </p>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-3 gap-8">
        <div
          v-for="(otherproject, index) in otherprojects"
          :key="otherproject.id"
          class="group relative bg-(--color-primaryalt) rounded-3xl overflow-hidden border backdrop-blur-sm hover:border-[#a73ee4] transition-all duration-500 hover:transform hover:-translate-y-2"
          :class="otherproject.bordColor"
          data-aos="fade-up"
          :data-aos-delay="(index + 1) * 100"
        >
          <div class="relative overflow-hidden">
            <img
              :src="otherproject.image"
              :alt="otherproject.title"
              class="w-full h-48 object-cover group-hover:scale-110 transition-transform duration-500"
            />
            <div
              class="absolute inset-0 bg-linear-to-t from-gray-900 via-transparent to-transparent"
            ></div>
            <div class="absolute top-4 right-4">
              <span
                class="px-3 py-1 text-white text-xs rounded-full font-semibold"
                :class="otherproject.badgeColor"
              >
                {{ otherproject.category }}
              </span>
            </div>
          </div>
          <div class="p-6">
            <h3
              class="text-xl font-bold text-white group-hover:text-(--color-sidealt) transition-colors duration-300"
            >
              {{ otherproject.title }}
            </h3>
            <p class="text-blue-100 text-sm leading-relaxed mb-4">
              {{ otherproject.desc }}
            </p>
            <div class="flex flex-wrap gap-2 mb-4">
              <span
                v-for="tech in otherproject.technolg"
                :key="tech"
                class="px-2 py-1 border rounded text-xs"
                :class="tech.class"
              >
                {{ tech.name }}
              </span>
            </div>
            <div class="flex gap-3">
              <a
                v-for="link in otherproject.links"
                :key="link.name"
                :href="link.url"
                target="_blank"
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
          <a
            href="https://github.com/ttPuck"
            target="_blank"
            class="px-8 py-4 border-pulse rounded-xl text-white font-semibold hover:shadow-lg hover:shadow-[#b14aed] hover:bg-amber-50 blob-glow transition-all duration-300 hover:scale-105 flex items-center"
          >
            View GitHub!

            <ArrowRightIcon class="w-5 h-5 ml-2" />
          </a>
          <button
            @click="scrollToContact"
            class="px-8 py-4 bg-(--color-side) cursor-pointer rounded-xl border-2 border-[#5386e4] text-white font-semibold hover:bg-text-white hover:bg-(--color-secondary) hover:shadow-lg hover:shadow-[#b14aed]/60 transition-all duration-300 flex items-center"
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
  const el = document.getElementById("contact");
  if (!el) return;

  el.scrollIntoView({ behavior: "smooth" });
};

const webprojects = ref([
  {
    id: 1,
    title: "Romans Road",
    desc: `A workout regimen web app inspired by Roman legionaries, with a focus on
        bodyweight and weight rucks. Built in Vue.js, and my handcrafted ManuCSS styling 
        for a worn down and aged Greek manuscript appearance.`,
    image: "../projects/project1.png",
    category: "Frontend",
    bordColor: "border-blue-500/30",
    badgeColor: "bg-(--color-secondary)",
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
        class: "text-white hover:text-[var(--color-secondary)]",
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
    image: "projects/project2.png",
    category: "Full-stack",
    bordColor: "border-blue-500/30",
    badgeColor: "bg-(--color-secondary)",
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
        class: "text-white hover:text-[var(--color-secondary)]",
      },
      {
        name: "Github Repo",
        url: "https://github.com/ttPuck/c2socket",
        icon: CodeBracketIcon,
        class: "text-white hover:text-[var(--color-secondary)]",
      },
    ],
  },
  {
    id: 3,
    title: "Dev Portfolio Template",
    desc: `A Github repository of this very website, built in Vue.js! Simply fork or download, and supply your own information and images, and customize to your liking! `,
    image: "projects/project7.png",
    category: "Frontend",
    bordColor: "border-blue-500/30",
    badgeColor: "bg-(--color-secondary)",
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
        url: "https://github.com/ttPuck/portfolio-clone",
        icon: ArrowDownTrayIcon,
        class: "text-white hover:text-[var(--color-secondary)]",
      },
    ],
  },
]);
const otherprojects = ref([
  {
    id: 1,
    title: "nvSIL",
    desc: `A faithful replica of nvALT (a successor to Notational Velocity) for Apple Silicon. Built in Swift using StoryBoard UI.`,
    image: "projects/project4.png",
    category: "App Development",
    bordColor: "border-blue-500/30",
    badgeColor: "bg-[#a600ff]",
    technolg: [
      {
        name: "Swift",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
    ],
    links: [
      {
        name: "Github Repo & Packaged App",
        url: "https://github.com/ptwees/nvSIL",
        icon: ArrowDownTrayIcon,
        class: "text-white hover:text-[var(--color-secondary)]",
      },
    ],
  },
  {
    id: 2,
    title: "nvSIL 2",
    desc: `A successor to my app, nvSIL. It features a new tab (subfolder) ability, allowing notes to be stored in subfolders, and a .md and TODO.txt syntax parser to enable a user access to all TODO's via a TODO tab.`,
    image: "projects/project6.png",
    category: "App Development",
    bordColor: "border-blue-500/30",
    badgeColor: "bg-[#a600ff]",
    technolg: [
      {
        name: "Swift",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
    ],
    links: [
      {
        name: "Github Repo & Packaged App",
        url: "https://github.com/ptwees/nvSIL",
        icon: ArrowDownTrayIcon,
        class: "text-white hover:text-[var(--color-secondary)]",
      },
    ],
  },
  {
    id: 3,
    title: "BREASTPLATE",
    desc: `A hyper realistic tactical, survival looter shooter in an apocalyptic world. Built in Godot, utilizing GDScript and C# and local hosting for multiplayer, it is a 3/4 shooter focusing on small unit tactics, CQB, and teambuilding.`,
    category: "Game Development",
    image: "projects/project5.png",
    bordColor: "border-blue-500/30",
    badgeColor: "bg-[#e67802]",
    technolg: [
      {
        name: "Godot (GDScript)",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
      {
        name: "C#",
        class: "bg-blue-500/20 border-blue-400/30 text-blue-200",
      },
    ],
    links: [
      {
        name: "Github Repo & Links To Game",
        url: "https://github.com/ttPuck/BREASTPLATE",
        icon: ArrowDownTrayIcon,
        class: "text-white hover:text-[var(--color-secondary)]",
      },
    ],
  },
]);
</script>
