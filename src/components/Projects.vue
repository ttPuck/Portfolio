<template >
    <section class="relative py-20 overflow-hidden" id="projects">
        <div class="relative z-10 max-w-8xl mx-auto px-4 sm:6
        lg:px-8">
        <div class="text-center mb-16" data-aos='fade-up'>
        <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
            My <span class="text-transparent bg-clip-text
            bg-linear-to-r from-blue-400 to-cyan-400">
                Projects
            </span>
        </h2>
        <p class="text-blue-200 text-lg max-w-2xl mx-auto">
            A collection of my projects, both public and private
        </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3
        gap-8">
        <div>

        </div>
        </div>
        </div>
    </section>
</template>
<script setup>
import { EyeIcon } from '@heroicons/vue/16/solid';
import { ref } from 'vue';


const projects = ref([
    {
        id:1,
        title: "C2 - A Discord inspired team communications web app",
        desc: `Full-stack Discord-style web application built 
        with Next.js 13 and React, featuring real-time 
        messaging via Socket.io, a MySQL database managed with Prisma, and a responsive UI styled with Tailwind CSS.`,
        image: '../public/project1.png',
        category: 'Full-stack',
        bordColor: 'border-blue-500/30',
        badgeColor: "bg-blue-500",
        technolg: [
            {
            name: "Next.js", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
             {
            name: "React", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
             {
            name: "Socket.io", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
              {
            name: "Clerk", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
              {
            name: "Prisma", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
              {
            name: "Tailwind CSS", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
        ],
        links: [
            {name: "Website (Sign-up and Login)", url: "#", icon: EyeIcon,
                class: 'text-white hover:text-blue-300'
            },
             {name: "Github Repo", url: "#", icon: EyeIcon,
                class: 'text-white hover:text-blue-300'
            },
        ]
    },
       {
        id:2,
        title: "",
        desc: `Full-stack Discord-style web application built 
        with Next.js 13 and React, featuring real-time 
        messaging via Socket.io, a MySQL database managed with Prisma, and a responsive UI styled with Tailwind CSS.`,
        image: '../public/project1.png',
        category: 'Full-stack',
        bordColor: 'border-blue-500/30',
        badgeColor: "bg-blue-500",
        technolg: [
            {
            name: "Next.js", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
             {
            name: "React", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
             {
            name: "Socket.io", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
              {
            name: "Clerk", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
              {
            name: "Prisma", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
              {
            name: "Tailwind CSS", 
            class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'},
        ],
        links: [
            {name: "Website (Sign-up and Login)", url: "#", icon: EyeIcon,
                class: 'text-white hover:text-blue-300'
            },
             {name: "Github Repo", url: "#", icon: EyeIcon,
                class: 'text-white hover:text-blue-300'
            },
        ]
    }



])
</script>
