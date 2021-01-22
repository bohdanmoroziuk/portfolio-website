<template>
  <section class="services section">
    <div class="services__container">
      <h2 class="services__title">{{ title }}</h2>
      <div class="services__grid">
        <div class="services__left">
          <Service
            v-for="service of services"
            :key="service.title"
            v-bind="service"
          />
        </div>
        <div class="services__right">
          <img class="services__image" :src="image.src" :alt="image.alt">
        </div>
      </div>
    </div>
    <EmailBar v-bind="emailBar" />
  </section>
</template>

<script>
import Service from '@/components/Service.vue';
import EmailBar from '@/components/EmailBar.vue';

export default {
  name: 'Services',
  props: {
    title: {
      type: String,
      required: true,
    },
    image: {
      type: Object,
      required: true,
    },
    services: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      emailBar: {
        title: 'Email',
        email: 'john.doe@gmail.com',
        image: {
          src: '/images/mail.svg',
          alt: 'mail icon',
        },
      },
    };
  },
  components: {
    Service,
    EmailBar,
  },
};
</script>

<style scoped>
.services {
  background: #002ed0;
  color: #fff;
  position: relative;
}

.services__container {
  background: #000;
  padding: 100px 0 100px 60px;
}

.services__grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  grid-template-rows: 700px;
}

.services__title {
  font-size: 50px;
}

.services__left {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  padding: 0 50px;
}

.services__image {
  height: 700px;
  width: 100%;
}

@media screen and (max-width: 768px) {
  .services__grid {
    grid-template-columns: 1fr;
  }

  .services__image {
    display: none;
  }
}

@media screen and (max-width: 468px) {
  .services__container {
    padding: 100px 0 160px 16px;
  }

  .services__grid {
    grid-template-columns: 1fr;
    grid-template-rows: 900px;
  }

  .services__title {
    text-align: center;
    margin-bottom: 50px;
  }

  .services__left {
    padding: 0 24px;
  }
}
</style>
