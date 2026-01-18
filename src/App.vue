<template >
  <div v-if="loading">
    <LoadingSpinner />
  
  </div>
  <div v-else class="min-h-screen bg-linear-to-br from-gray-900
  via-blue-900 to-gray-900">
<NavBar />
<MeSection />
<Services /> 
<AboutMe />
<ExperienceSkills />
<Projects />
<Contact />
<Testimonials />
<Footer />
<BackToTop />
</div>
</template>
<script>

import Aos from 'aos';
import 'aos/dist/aos.css';
import MeSection from './components/MeSection.vue';
import NavBar from './components/NavBar.vue';
import {ref, nextTick, onMounted } from 'vue';
import Services from './components/Services.vue';
import AboutMe from './components/AboutMe.vue';
import ExperienceSkills from './components/ExperienceSkills.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';
import Testimonials from './components/Testimonials.vue';
import Footer from './components/Footer.vue';
import BackToTop from './components/BackToTop.vue';
import LoadingSpinner from './components/LoadingSpinner.vue';

export default {
components : {
    NavBar, 
  MeSection,
  Services,
  AboutMe,
  ExperienceSkills,
  Projects,
  Contact,
  Testimonials,
  Footer,
  BackToTop,
  LoadingSpinner
},
setup() {
  const loading = ref(true);
  onMounted(async () => {
    await nextTick();
    Aos.init({
      duration: 900,
      once: false,
      offset: 100,
      easing: 'ease-in-out',
    });
setTimeout(() => {
  loading.value = false;

}, 800);
  });
  return {loading};


}
}
</script>
