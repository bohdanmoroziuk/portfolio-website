<template>
  <div class="home">
    <Hero v-bind="hero" />
    <About v-bind="about" />
    <Services v-bind="services" />
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue';
import About from '@/components/About.vue';
import Services from '@/components/Services.vue';

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
      services: {
        title: 'Services',
        image: {
          src: '/images/macbook.png',
          alt: 'macbook',
        },
        services: [
          {
            title: 'UX Strategy',
            icon: '/images/chess.svg',
            description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit.',
          },
          {
            title: 'UX Strategy',
            icon: '/images/wireframe.svg',
            description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit.',
          },
          {
            title: 'UX Strategy',
            icon: '/images/virtual.svg',
            description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit.',
          },
        ],
      },
    };
  },
  components: {
    Hero,
    About,
    Services,
  },
};
</script>
