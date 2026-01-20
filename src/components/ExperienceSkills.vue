<template>
  <section class="relative py-20 overflow-hidden" id="skills">
    <div class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16" data-aos="fade-up">
        <h2 class="text-4xl md:text-5xl font-bold text-blue-200 mb-4">
          <span
            class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400"
          >
            Skills
          </span>
          & Experience
        </h2>
        <p class="text-white text-lg max-w-2xl mx-auto">
          My Technical Cataloge And Professional Journey
        </p>
      </div>
      <div class="grid lg:grid-cols-2 gap-12 lg:gap-16">
        <div data-aos="fade-right">
          <h3
            class="text-2xl font-bold text-white mb-8 flex items-center gap-3"
          >
            Technical Skills
          </h3>
          <div class="space-y-6">
            <div v-for="skill in skills" :key="skill.id" class="group">
              <div class="flex items-center justify-between mb-3">
                <span class="text-white font-semibold flex items-center gap-2">
                  <component
                    :is="skill.icon"
                    class="w-5 h-5"
                    :class="skill.iconColor"
                  ></component>
                  {{ skill.title }}
                </span>
              </div>
              <div class="flex flex-wrap gap-1">
                <span
                  v-for="t in skill.tech"
                  :key="t.name"
                  class="px-2 py-2 bg-linear-to-r from-blue-500/20 border border-blue-400/30 rounded-full text-white text-sm font-medium hover:scale-105 transition-transform duration-300"
                >
                  {{ t.name }}
                </span>
              </div>
              <div class="mt-3 h-2 bg-gray-700 rounded-full overflow-hidden">
                <div
                  class="h-full rounded-full transition-all duration-1000 group-hover:scale-105"
                  :class="skill.gradient"
                  :style="{ width: skill.percentage + '%' }"
                ></div>
              </div>
            </div>
          </div>
          <div class="mt-12">
            <div class="flex flex-wrap gap-3">
              <span
                v-for="tech in techStack"
                :key="tech"
                class="px-4 py-2 bg-linear-to-r from-blue-500/20 border border-blue-400/30 rounded-full text-white text-sm font-medium hover:scale-105 transition-transform duration-300"
              >
                {{ tech }}
              </span>
            </div>
          </div>
        </div>
        <div data-aos="fade left">
          <h3
            class="text-2xl font-bold text-white mb-8 flex items-center gap-3"
          >
            <BriefcaseIcon class="w-8 h-8 text-cyan-400" />
            Work Experience
          </h3>
          <div class="space-y-8">
            <div
              v-for="exp in experiences"
              :key="exp.id"
              class="relative pl-8 border-1-2 group"
              :class="exp.borderColor"
            >
              <div
                class="absolute -left-2 top-0 w-4 h-4 rounded-full group-hover:scale-150 transition-transform duration-300"
                :class="exp.dotColor"
              ></div>
              <div
                class="bg-linear-to-br from gray-800/50 to-blue-900/30 rounded-2xl p-6 border backdrop-blur-sm group-hover:border-blue-400/40 transition-all duration-300"
                :class="exp.borderClass"
              >
                <div
                  class="flex flex-col sm:flex-row sm:items-center sm:jusitfy-between mb-3"
                >
                  <h4 class="text-lg font-bold text-white">
                    {{ exp.position }}
                  </h4>
                  <span :class="exp.dateColor" class="mt-1 sm:mt-0">{{
                    exp.period
                  }}</span>
                </div>
                <p :class="exp.companyColor" class="font-medium mb-3">
                  {{ exp.company }}
                </p>
                <p class="text-blue-100 text-sm leading-relaxed">
                  {{ exp.desc }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import {
  BriefcaseIcon,
  CloudIcon,
  CodeBracketIcon,
  DevicePhoneMobileIcon,
  PaintBrushIcon,
  ServerIcon,
  Squares2X2Icon,
} from "@heroicons/vue/16/solid";
const tech = {
  vue: { name: "Vue.js" },
  react: { name: "React" },
  next: { name: "Next.js" },
  node: { name: "Node.js" },
  swift: { name: "Swift" },
  objectivec: { name: "Objective-C" },
  appkit: { name: "AppKit" },
  mongo: { name: "MongoDB" },
  postgres: { name: "PostgreSQL" },
  supabase: { name: "Supabase" },
  tailwind: { name: "Tailwind CSS" },
  git: { name: "Git" },
  figma: { name: "Figma" },
};

const skills = [
  {
    id: 1,
    title: "Frontend Development",
    icon: CodeBracketIcon,
    iconColor: "text-blue-400",
    percentage: 95,
    percentageColor: "text-blue-400 text-sm",
    gradient: "bg-linear-to-r from-blue-500 to-cyan-500",
    tech: [tech.vue, tech.react, tech.next, tech.objectivec, tech.appkit],
  },
  {
    id: 2,
    title: "Backend Development",
    icon: ServerIcon,
    iconColor: "text-cyan-400",
    percentage: 85,
    percentageColor: "text-blue-400 text-sm",
    gradient: "bg-linear-to-r from-blue-500 to-cyan-500",
    tech: [tech.mongo, tech.supabase, tech.node, tech.postgres],
  },
  {
    id: 3,
    title: "Mobile Development",
    icon: DevicePhoneMobileIcon,
    iconColor: "text-blue-400",
    percentage: 75,
    percentageColor: "text-blue-400 text-sm",
    gradient: "bg-linear-to-r from-blue-500 to-cyan-500",
    tech: [tech.swift, tech.objectivec, tech.appkit],
  },
  {
    id: 4,
    title: "UI/UX Design",
    icon: PaintBrushIcon,
    iconColor: "text-cyan-400",
    percentage: 70,
    percentageColor: "text-blue-400 text-sm",
    gradient: "bg-linear-to-r from-blue-500 to-cyan-500",
    tech: [tech.tailwind, tech.figma],
  },
  {
    id: 5,
    title: "Team Development & Remote Operations",
    icon: CloudIcon,
    iconColor: "text-cyan-400",
    percentage: 70,
    percentageColor: "text-blue-400 text-sm",
    gradient: "bg-linear-to-r from-blue-500 to-cyan-500",
  },
];
const experiences = [
  {
    id: 1,
    position: "Freelance Full-Stack Developer ",
    company: "Garbero Media",
    period: " 2025 - Present",
    desc: "Full-stack developer and UI/UX design for multiple websites, the major being a photography portfolio and booking website built with Vue.js and a Node.js backend, featuring a MongoDB customer database and responsive UI. Integrated Plaid Link on the frontend with secure server-side Plaid API workflows for bank-linked payments. Implemented booking, scheduling, and transaction management using RESTful APIs.",
    borderColor: "border-blue-500/30",
    dotColor: "bg-blue-500",
    borderClass: "botder-blue=500/20",
    dateColor: "text-blue-400 text-sm font-semibold",
    companyColor: "text-cyan-400",
  },
  {
    id: 2,
    position: "Frontend Developer & Administrative Manager",
    company: "Faith Talent Services",
    period: "2019 - 2025",
    desc: "Frontend developer and UI/UX design for one recruiting website, and manager of all HR and administrative duties for the company. Duties included: Onboarding, Payroll, Calendar Management, Administrative Tasks, and Clerical Tasks.",
    borderColor: "border-blue-500/30",
    dotColor: "bg-blue-500",
    borderClass: "botder-blue=500/20",
    dateColor: "text-blue-400 text-sm font-semibold",
    companyColor: "text-cyan-400",
  },
];
</script>
