<template>
  <div class="home">
    <Hero v-bind="hero" />
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue';

export default {
  name: 'Home',
  data() {
    return {
      hero: {
        user: '01 - John Doe',
        title: 'User Experience Designer',
        description: 'I have years of experiance working with small and large companies and I\'m currently looking for the new opportunity.',
      },
    };
  },
  components: {
    Hero,
  },
};
</script>
