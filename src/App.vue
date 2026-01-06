<template >
  <div class="min-h-screen bg-linear-to-br from-gray-900
  via-blue-900 to-gray-900">
<NavBar />
<MeSection />
 
</div>
</template>
<script>

import Aos from 'aos';
import 'aos/dist/aos.css';
import MeSection from './components/MeSection.vue';
import NavBar from './components/NavBar.vue';
import {ref, nextTick, onMounted } from 'vue';

export default {
components : {
    NavBar, 
  MeSection,
},
setup() {
  const loading = ref(true);
  onMounted(async () => {
    await nextTick();
    Aos.init({
      duration: 900,
      once: false,
      offest: 100,
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
