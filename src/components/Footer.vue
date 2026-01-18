<template >
    <footer class="relative bg-gray-700/60 border-t
    border-blue-500/20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 py-12">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
            <div class="md:col-span-2">
                <div class="text-2xl font-bold bg-linear-to-r
                from-blue-400 to-cyan-400 bg-clip-text
                text-transparent mb-4">
                Ian.dev
                </div>
                <p class="text-blue-300 text-sm leading-relaxed
                max-w-md">
                    Love the Lord your 
                    God with all your heart and with 
                    all your soul and with all your mind
                     and with all your strength.
                </p>
                <div class="flex gap-4 mt-6">
                    <a href="#" class="p-2 bg-blue-500/40
                    border border-blue-400/30 rounded-lg
                    text-blue-400 hover:bg-blue-500/30
                    transition-all">
                    <EnvelopeIcon class="w-5 h-5" />
          </a>
                        <a href="#" class="p-2 bg-blue-500/40
                    border border-blue-400/30 rounded-lg
                    text-blue-400 hover:bg-blue-500/30
                    transition-all">
                    <MapIcon class="w-5 h-5" />
                </a>
                </div>
            </div>
            <div>
                <h3 class="text-white font-semibold mb-4">
                    Quick Links
                </h3>
                <ul class="space-y-2">
                    <li v-for="link in quickLinks"
                    :key="link.name"
                    >
                        <a 
                        :href="link.href"
                        class="text-blue-200 hover:text-blue-400
                        text-sm transition-colors">
                    {{ link.name }}
                    </a>
                    </li>
                </ul>
            </div>
            <div>
                <h3 class="text-white font-semibold mb-4">
                    Services</h3>
                    <ul class="space-y-2">
                        <li
                        v-for="service in services"
                        :key="service">
                        <a href="#"
                        class="text-blue-200 hover:text-blue-400
                        text-sm transition-colors">
                    {{ service }}
                    </a>
                        </li>
                    </ul>
            </div>
        </div>
        <div
        class="border-t border-blue-600/50 mt-8 pt-8 flex
        flex-col md:flex-row justify-between items-center">
        <p class="text-blue-300 text-sm">
            @ 2026 Ian. All rights reserved
        </p>
        </div>
    </div>
 </footer>
</template>
<script setup>
import { 
    EnvelopeIcon, 
    MapIcon } from '@heroicons/vue/16/solid';

    const quickLinks = [
        {name: "Home", href: "#home"},
        {name: "About", href: "#about"},
        {name: "Services", href: "#services"},
        {name: "Projects", href: "#projects"},
        {name: "Testimonials", href: "#testimonials"},
         {name: "Contact", href: "#contact"},
       

    ]
const services = [
    'Web Development', 
   'Mobile Development', 
    'UI/UX Design', 
    'Technical Writing', 
    'Content Specialist'

]
</script>
