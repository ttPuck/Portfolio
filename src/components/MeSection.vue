<template>
  <section
    class="relative w-full overflow-hidden min-h-screen flex items-center"
  >
    <div
      class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto relative z-10"
    >
      <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
        <div class="flex flex-col md:mt-0 mt-20 justify-center">
          <div class="text-white lg:text-left" data-aos="fade-right">
            <h1
              class="text-white font-bold text-4xl md:text-5xl lg:text-6xl leading-tight"
            >
              Hey, I'm
              <span
                class="text-transparent bg-clip-text bg-linear-to-r from-red-500 to-orange-200"
                >Ian </span
              >😀
            </h1>
            <p
              class="text-blue-200 font-medium text-lg md:text-xl mt-4"
              data-aos="fade-right"
              data-aos-delay="80"
            ></p>
            <p>Full-Stack Developer & Content Specialist</p>
          </div>
          <p
            class="text-gray-300 pt-6 text-center lg:text-left mx-auto max-w-xl text-lg leading-relaxed"
          >
            I was eyes to the blind, and feet was I to the lame. 16I was a
            father to the poor: and the cause which I knew not I searched out.
            17And I brake the jaws of the wicked, and plucked the spoil out of
            his teeth.
          </p>
          <div
            class="flex items-center gap-4 pt-8 flex-col 
            sm:flex-row sm:w-max sm:mx-auto lg:mx-0"
          data-aos="fade-up"
          data-aos-delay="450">
          <button
          class="px-8 md:px-10 py-4 rounded-x1 relative group
          w-full sm:w-max flex justify-center overflow-hidden
           bg-linear-to-r from-red-400 to-blue-800
           hover:from-white-500 hover:to-blue-600 transition-all
           duration-300"
           >
            <span class="relative flex items-center 
            justify-center text-white font-semibold
            text-lg" >
              Reach out to me
              <ArrowRightIcon class="ml-2 w-5 h-5
            group-hover:translate-x-1 transition-transform" />
            </span>
            </button>
            <button
            class="border-2 border-blue-400 px-8 md:px-10
            py-4 rounded-xl relative troup w-full sm:w-max
            flex justify-center hover:bg-blue-400/10
            transition-all duration-300
            ">
            <div class="flex items-center justify-center relative">
              <ArrowDownTrayIcon
              class="w-5 h-5 text-white 
              group-hover:translate-y-1 transition/transform" />
              <span class="pl-3 text-white font-semibold
              text-lg">
                Download CV
              </span>
            </div>
            </button>
        </div>
        <div class="flex items-center justify-center 
        lg:justify-start gap-7 pt-12"
        data-aos="fade-up" data-aos-delay="300">
        <div class="text-center">
          <div class="text-2xl font-bold text-blue-400">50+</div>
          <div class="text-blue-200 text-sm" >Projects</div>
        </div>
          <div class="text-center">
          <div class="text-2xl font-bold text-blue-400">2+</div>
          <div class="text-blue-200 text-sm" >Years</div>
        </div>
          <div class="text-center">
          <div class="text-2xl font-bold text-blue-400">30+</div>
          <div class="text-blue-200 text-sm" >Clients</div>
        </div>
        </div>
        </div>
        <!-- Profile Image-->
        <div class="lg:h-full flex justify-center lg:justify-end">
          <div class="relative w-full max-w-md lg:max-w-lg">
            <div class="relative z-10 bg-linear-to-r
            from-blue-600 to-cyan-500 shadow-2xl
            rounded-[50%_40%_30%_60%/60%_30%_70%_30%]
            p-4 backdrop-blur-sm border border-orange-600/30
            -translate-y-6" 
            data-aos="zoom-in" data-aos-delay="450">
            <div class="reounded-xl overflow-hidden" >
              <img 
              src="../../public/Ian.png" 
              alt="Ian - Profile Image"
              loading="lazy"
              class="w-[50px] h-[500px] object-contain
              -translate-y-8">
            </div>
               </div>
               <div class="absolute" >

               </div>
          </div>

        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ArrowDownTrayIcon, ArrowRightIcon } from '@heroicons/vue/16/solid';


</script>

