<template>
  <div class="home">
    <Hero v-bind="hero" />
    <About v-bind="about" />
    <Services v-bind="services" />
    <Portfolio v-bind="portfolio" />
    <Footer v-bind="footer" />
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue';
import About from '@/components/About.vue';
import Services from '@/components/Services.vue';
import Portfolio from '@/components/Portfolio.vue';
import Footer from '@/components/Footer.vue';

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
      portfolio: {
        projects: [
          {
            name: 'Project 1',
            image: {
              src: '/images/portfolio-1.svg',
              alt: 'Project 1',
            },
          },
          {
            name: 'Project 2',
            image: {
              src: '/images/portfolio-2.svg',
              alt: 'Project 2',
            },
          },
          {
            name: 'Project 3',
            image: {
              src: '/images/portfolio-3.svg',
              alt: 'Project 3',
            },
          },
        ],
      },
      footer: {
        author: 'John Doe',
        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni, recusandae?',
        nav: [
          { name: 'About', to: '/' },
          { name: 'Services', to: '/' },
          { name: 'Portfolio', to: '/' },
        ],
      },
    };
  },
  components: {
    Hero,
    About,
    Services,
    Portfolio,
    Footer,
  },
};
</script>
