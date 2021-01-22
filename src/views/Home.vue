<template>
  <div class="home">
    <Hero v-bind="hero" />
    <About v-bind="about" />
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue';
import About from '@/components/About.vue';

export default {
  name: 'Home',
  data() {
    return {
      hero: {
        user: '01 - John Doe',
        title: 'User Experience Designer',
        description: 'I have years of experiance working with small and large companies and I\'m currently looking for the new opportunity.',
      },
      about: {
        title: 'Hello, I\'m John',
        subtitle: 'I am John Doe, a UI/UX Consultant currently living in San Franciso, CA.',
        description: `Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolores,
          nesciunt necessitatibus nobis nisi voluptate suscipit, quaerat officia
          unde obcaecati non aut quod. Nihil commodi eius nesciunt assumenda impedit
          doloremque repudiandae!`,
      },
    };
  },
  components: {
    Hero,
    About,
  },
};
</script>
