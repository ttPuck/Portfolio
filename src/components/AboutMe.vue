<template>
  <section
    class="relative py-20 overflow-hidden min-h-screen flex items-center"
    id="about"
  >
    <div
      class="w-full px-5 sm:px-12 md:px-14 lg:px-18 max-w-7xl lg:max-w-10xl mx-auto relative z-10"
    >
      <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
        <div
          class="lg:h-full flex justify-center lg:justify-start order-2 lg:order-1"
        >
          <div class="relative w-full max-w">
            <div
              data-aos="zoom-in"
              class="relative bg-(--color-secondaryalt)  rounded-3xl p-6 backdrop-blur-sm border border-blue-500/30 shadow-2xl"
            >
              <div class="grid grid-cols-2 gap-4">
                <div
                  v-for="(image, index) in aboutImage"
                  :key="image.id"
                  class="relative group"
                  :data-aos="image.animation"
                  :data-aos-delay="image.delay"
                >
                  <div
                    class="rounded-2xl p-2 border shadow-lg"
                    :class="image.gradient"
                  >
                    <img
                      :src="image.src"
                      :alt="image.alt"
                      class="w-full h-48 object-cover rounded-xl group-hover:scale-105 transition-transform duration-300"
                    />
                  </div>
                  <div
                    class="absolute -top-2 -right-2 text-white text-xs px-2 py-1 rounded-full font-semibold"
                    :class="image.badgeColor"
                  >
                    {{ image.badge }}
                  </div>
                </div>
              </div>
              <div
                class="absolute -bottom-4 left-1/2 transform -translate-x-1/2 z-20 bg-(--color-side)  rounded-2xl px-6 py-3 border border-blue-400/40 shadow-xl"
                data-aos="fade-up"
                data-aos-delay="600"
              >
                <div class="text-center text-black text-xl font-bold">
                  2+ Years Experience
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="flex flex-col justify-center order-1 lg:order-2">
          <div class="text-center lg:text-left" data-aos="fade-left">
            <h2
              class="text-transparent bg-clip-text bg-linear-to-r from-[#454ade] to-[#b14aed] font-bold text-4xl md:text-5xl lg:text-6xl leading-tight"
            >
              About
              <span 
                class="text-black"
              >
                Me</span
              > 
            </h2>
            <p
              class="text-black font-medium text-lg md:text-xl mt-4"
              data-aos="fade-left"
              data-aos-delay="400"
            >
              Full-Stack Developer
            </p>
          </div>
          <div
            class="grid grid-cols-1 sm:grid-cols-2 gap-6 pt-8"
            data-aos="fade-up"
            data-aos-delay="300"
          >
            <div v-for="skill in skills" :key="skill.id" class="flex flex-col">
              <div class="flex items-center gap-3 mb-3">
                <component
                  :is="skill.icon"
                  class="w-6 h-6"
                  :class="skill.iconColor"
                ></component>
                <h3 class="text-lg font-bold text-black">
                  {{ skill.title }}
                </h3>
              </div>
              <p class="text-black text-sm">
                {{ skill.desc }}
              </p>
            </div>
          </div>
          <div
            class="flex gap-4 pt-8 flex-col sm:flex-row"
            data-aos="fade-up"
            data-aos-delay="400"
          >
            <button
              v-for="button in ctaButtons"
              :key="button.id"
              class="px-8 py-3 rounded-xl bg-(--color-primaryalt) font-semibold transition-all duration-300 flex items-center justify-center hover:shadow-lg hover:shadow-[#b14aed]/60"
              :class="button.classes"
             @click="button.text === 'Contact Me' && scrollToContact() ; button.text === 'View Portfolio' ? scrollToProjects() : null"

            >
              <component
                :is="button.icon"
                class="w-4 h-4"
                :class="button.iconclass"
              />
              {{ button.text }} 
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
  const scrollToContact = () => {
  const el = document.getElementById("contact")
  if (el) {
    el.scrollIntoView({ behavior: "smooth" })
  }
}
import {
  ChatBubbleLeftRightIcon,
  CodeBracketSquareIcon,
  CubeIcon,
  PaintBrushIcon,
  ArrowRightIcon,
  ServerIcon,
} from "@heroicons/vue/16/solid";
import about1 from "/about1.png";
import about2 from "/about2.png";
import about3 from "/about3.png";
import about4 from "/about4.png";

  const scrollToProjects = () => {
  const el = document.getElementById("projects")
  if (!el) return 
  el.scrollIntoView({ behavior: "smooth" })
  }
const aboutImage = [
  {
    id: 1,
    src: about1,
    alt: "Pro",
    gradient: `bg-black
         border-blue-400/40`,
    badge: "Web Developer",
    badgeColor: "bg-[var(--color-primary)]",
    animation: "fade-right",
    delay: 200,
  },
  {
    id: 2,
    src: about2,
    alt: "",
    gradient: `bg-black
         border-blue-400/40`,
    badge: "App Developer",
    badgeColor: "bg-[var(--color-primary)]",
    animation: "fade-left",
    delay: 200,
  },
  {
    id: 3,
    src: about3,
    alt: "Pro",
    gradient: `bg-black
         border-blue-400/40`,
    badge: "Professional",
    badgeColor: "bg-[var(--color-primary)]",
    animation: "fade-right",
    delay: 400,
  },
  {
    id: 4,
    src: about4,
    alt: "Design",
    gradient: `bg-black
         border-blue-400/40`,
    badge: "Designer",
    badgeColor: "bg-[var(--color-primary)]",
    animation: "fade-left",
    delay: 400,
  },
];

const skills = [
  {
    id: 1,
    icon: CodeBracketSquareIcon,
    iconColor: "text-[var(--color-secondaryalt)]",
    title: "Frontend",
    desc: "JavaScript, Vue.js, React, Next.js, TypeScript, Tailwind CSS",
  },
  {
    id: 2,
    icon: ServerIcon,
    iconColor: "text-[var(--color-secondaryalt)]",
    title: "Backend",
    desc: "Node.js, MongoDB, Supabase, Cloudflare, SQL",
  },
  {
    id: 3,
    icon: PaintBrushIcon,
    iconColor: "text-[var(--color-secondaryalt)]",
    title: "Design",
    desc: "UI/UX Design, Photoshop, Figma, Prototyping",
  },
  {
    id: 4,
    icon: CubeIcon,
    iconColor: "text-[var(--color-secondaryalt)]",
    title: "Tools Used",
    desc: "Git, VSCode, Xcode, Vite, Hosting Services ",
  },
];

const ctaButtons = [
  {
    id: 1,
    text: "View Portfolio",
    icon: ArrowRightIcon,
    iconclass: `ml-2 group-hover:translate-x-1
        transition-transform`,
    classes: `bg-[var(--color-secondary)]
        text-white hover:bg-[var(--color-primary)] cursor-pointer`,
        
  },
  {
    id: 2,
    text: "Contact Me",
    icon: ChatBubbleLeftRightIcon,
    iconclass: `mr-2`,
    classes: `border border-[#454ade] text-white cursor-pointer
        hover:bg-[var(--color-secondary)] `,
  },
];
</script>
