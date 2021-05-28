<template>
  <div class="home">
    <HeroSection />
    <FormSection />
    <Services />
    <News />
  </div>
</template>

<script>

import HeroSection from '../components/HeroSection.vue'
import FormSection from '../components/FormSection.vue'
import Services from '../components/Services.vue'
import News from '../components/News.vue'

export default {
  name: 'Home',
  components: {
    HeroSection,
    FormSection,
    Services,
    News
  }
}
</script>
