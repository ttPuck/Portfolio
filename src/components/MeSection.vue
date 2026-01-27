<template>
  <section
    class="relative w-full overflow-hidden min-h-screen flex items-center"
  >
    <div
      class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto relative z-10"
    >
      <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
            <!-- Profile Image-->
          <div class="lg:h-full flex justify-center lg:justify-center">
          <div class="relative w-full max-w-md lg:max-w-lg">
            <div
              class="relative z-10 bg-linear-to-r from-[#501f6d] to-[#2e3194] shadow-2xl rounded-[40%_20%_30%_80%/10%_20%_30%_30%] p-4 backdrop-blur-sm border border-[#b14aed] -translate-y-6"
              data-aos="zoom-in"
              data-aos-delay="450"
            >
              <div class="rounded-xl overflow-hidden">
                <img
                  src="../../public/Ian.png"
                  alt="Ian - Profile Image"
                  loading="lazy"
                  class="w-[400px] h-[500px] object-contain -translate-y-7 translate-x-8 rounded-[20%]"
                />
              </div>
            </div>
            <div
              class="absolute -top-2 -right-4 w-10 h-10 bg-red-400 rounded-full blur-sm opacity-6 animate-pulse"
            ></div>
          </div>
        </div>
        <div class="flex flex-col md:mt-0 mt-20 justify-center">
          <div class="text-white lg:text-left" data-aos="fade-right">
            <h1
              class="text-white font-bold text-4xl md:text-5xl lg:text-6xl leading-tight"
            >
              Hey, I'm
              <span 
                class="text-transparent bg-clip-text bg-linear-to-r from-[#b14aed] to-[#454ade]"
                >Ian </span
              >😀
            </h1>
            <p
              class="text-white font-medium text-lg md:text-xl mt-4"
              data-aos="fade-right"
              data-aos-delay="80"
            ></p>
            <p>Full-Stack Developer</p>
          </div>
          <p
            class="font-light text-white pt-6 text-center lg:text-left mx-auto max-w-xl text-lg leading-relaxed"
            data-aos="fade-right"
            data-aos-delay="150"
          >
            I am an experienced frontend and backend developer of 2+ years, with
            a handful of projects under my belt. I specialize in Vue.js, Next.js, React, along with their complimentary backend tools
            such as MongoDB, Supabase, and Cloudflare. I would love to be part of a team
            where I could deliver effective and efficient code and provide my
            gifts and skills to any project that may need them!
          </p>
          <div
            class="flex items-center gap-4 pt-8 flex-col sm:flex-row sm:w-max sm:mx-auto lg:mx-0"
            data-aos="fade-up"
            data-aos-delay="450"
          >
          <div class="p-[2px] bg-gradient-to-r from-[#b14aed] to-[#454ade] rounded-xl w-full sm:w-max">
            <button
              @click="scrollToContact"
              class="px-8 md:px-10 py-4 rounded-xl relative group w-full sm:w-max flex justify-center overflow-hidden 
              bg-linear-to-r from-[#0b132b] to-[#0b132b] hover:from-[#b14aed] hover:to-[#454ade] cursor-pointer transition-all duration-300 bg-gray-900"
            >
            
              <span
                class="relative flex items-center justify-center text-white font-semibold text-lg"
              >
                Reach out to me
                <ArrowRightIcon
                  class="ml-2 w-5 h-5 group-hover:translate-x-1 transition-transform"
                />
              </span>
            </button>
            </div>
            <a href="/Ian.Portfolio.pdf" download>
          <!-- Gradient wrapper -->
<div class="p-[2px] bg-gradient-to-r from-[#b14aed] to-[#454ade] rounded-xl w-full sm:w-max">
  <!-- Inner button -->
  <button class="px-8 md:px-10 py-4 rounded-xl relative group w-full flex justify-center hover:bg-blue-400/10 transition-all duration-300 bg-gray-900">
    <div class="flex items-center justify-center relative cursor-pointer">
      <ArrowDownTrayIcon class="w-5 h-5 text-white group-hover:translate-y-1 transition-transform" />
      <span class="pl-3 text-white font-semibold text-lg">
        Download CV
      </span>
    </div>
  </button>
</div>
            </a>
          </div>
          <div
            class="flex items-center justify-center lg:justify-start gap-7 pt-12"
            data-aos="fade-up"
            data-aos-delay="300"
          >
            <div class="text-center">
              <div class="text-2xl font-bold text-[#e5f4e3]">4</div>
              <div class="text-white text-sm">Projects</div>
            </div>
            <div class="text-center">
              <div class="text-2xl font-bold text-[#e5f4e3]">2+</div>
              <div class="text-white text-sm">Years</div>
            </div>
            <div class="text-center">
              <div class="text-2xl font-bold text-[#e5f4e3]">2+</div>
              <div class="text-white text-sm">Clients</div>
            </div>
          </div>
        </div>
        <!-- Profile Image-->
     
      </div>
    </div>
  </section>
</template>

<script setup>
import { ArrowDownTrayIcon, ArrowRightIcon } from "@heroicons/vue/16/solid";
const scrollToContact = () => {
  const el = document.getElementById("contact")
  if (!el) return

  el.scrollIntoView({ behavior: "smooth" })
}
</script>
