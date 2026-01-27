<template>
  <section class="relative py-20 overflow-hidden" id="services">
    <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center m-16" data-aos="fade-up">
        <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
          My
          <span
            class="text-transparent bg-clip-text bg-linear-to-r from-[#b14aed] to-[#454ade]"
          >
            Services
          </span>
        </h2>
        <p
          class="text-white text-lg max-w-2xl mx-auto"
          data-aos="fade-up"
          data-aos-delay="80"
        >
         My Skill Sets To Provide You And Your Team With Amazing Services
        </p>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5">
        <div
          v-for="(service, index) in services"
          :key="service.id"
          :data-aos="'fade-up'"
          :data-aos-delay="index * 100 + 200"
          class="group relative p-14 rounded-2xl bg-linear-to-br from-gray-800/50 to-blue-900/30 backdrop-blur-sm border border-[#5386e4] hover:border-[#a73ee4] transition-all duration-500 hover:transform hover:-translate-y-2"
        >
          <div
            class="absolute inset-0 bg-linear-to-r from-blue-500/5 to-cyan-500/5 rounded-2xl opacity-0 duration-500 group-hover:opacity-100 transition-opacity"
          ></div>
          <div class="relative z-10 mb-6">
            <div
              class="inline-flex items-center justify-center w-16 h-16 rounded-xl bg-linear-to-r from-blue-500/20 to-cyan-500/20 border border-blue-400/30 group-hover:scale-110 transition-transform duration-300"
            >
              <component
                :is="service.icon"
                class="w-8 h-8 text-[#5386e4]"
              ></component>
            </div>
          </div>
          <p class="text-white font-bold absolute bottom-6 left opacity-0 group-hover:opacity-100 transform translate-x-4 group-hover:translate-x-[-200] transition-all duration-300">See Projects With This Service!</p>
          <div class="relative z-10">
            <h3
              class="text-xl font-bold text-white mb-3 group-hover:text-[#b14aed] transition-colors duration-300"
            >
              {{ service.name }}
            </h3>
            <p class="text-white leading-relaxed">
              {{ service.desc }}
            </p>
          </div>
          <div
            class="absolute bottom-6 right-6 opacity-0 cursor-pointer group-hover:opacity-100 transform translate-x-4 group-hover:translate-x-0 transition-all duration-300"
          > <button @click="scrollToProjects">
            <ArrowRightIcon  class="w-6 h-6 text-cyan-400 cursor-pointer" />
            </button>
          </div>
        </div>
      </div>
      <div class="text-center mt-16" data-aos="fade-up" data-aos-delay="200">
        <div class="inline-flex flex-col sm:flex-row gap-4 items-center">
          <button
           @click="scrollToContact"
            class="px-8 py-4 rounded-xl border-pulse text-white font-semibold hover:bg-[#0b132b]/50 hover:shadow-lg hover:shadow-[#b14aed]/60 cursor-pointer transition-all duration-300 flex items-center"
          >
            Get In Touch
            <ChatBubbleLeftRightIcon class="w-5 h-5 ml-2" />
          </button>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
  const scrollToContact = () => {
  const el = document.getElementById("contact")
  if (!el) return
   el.scrollIntoView({ behavior: "smooth" })}
  const scrollToProjects = () => {
  const el = document.getElementById("projects")
  if (!el) return 
  el.scrollIntoView({ behavior: "smooth" })
  }
import {
  ArrowRightIcon,
  ChatBubbleLeftRightIcon,
  CodeBracketIcon,
  DocumentTextIcon,
  EnvelopeIcon,
} from "@heroicons/vue/16/solid";
import { ref } from "vue";

const services = ref([
  {
    id: 1,
    icon: CodeBracketIcon,
    name: "Web Development",
    desc: `I am able to provide efficient and amazing websites and webapps with my experience in JavaScript 
    frameworks and their backend complements such as MongoDB, Supabase, and Cloudflare.`,
  },
  {
    id: 2,
    icon: DocumentTextIcon,
    name: "Technical Writing",
    desc: `With surprising ease, I can distill complex and hard-to-understand topics and subjects into a neatly packaged 
    and easy-to-comprehend source books, teaching material, or general knowledge transfer.`,
  },
  {
    id: 4,
    icon: EnvelopeIcon,
    name: "Administrative Services",
    desc: `With overwhelming experience, I am able to provide any form of administrative services, such as technical writing, clerical and management tasks.`,
  },
]);
</script>
