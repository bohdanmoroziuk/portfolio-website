<template>
  <section class="about section">
    <div class="about__container">
      <h2 class="about__title">{{ title }}</h2>
      <div class="about__content">
        <div class="about__text">
          <h3 class="about__subtitle">{{ subtitle }}</h3>
          <p class="about__description">{{ description }}</p>
        </div>
        <div class="about__image-wrapper">
          <img class="about__image" src="/images/profile.png" alt="profile">
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'About',
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.about {
  padding: 60px;
  background: #002ed0;
  color: #fff;
}

.about__container {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.about__title {
  font-size: 110px;
  color: #fff;
  -webkit-text-fill-color: transparent;
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: #fff;
  margin-bottom: 32px;
}

.about__content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 700px;
}

.about__text {
  padding-right: 20px;
}

.about__subtitle {
  font-size: 48px;
  line-height: 1.5;
  margin-bottom: 32px;
}

.about__description {
  line-height: 2.4;
}

.about__image-wrapper {
  display: flex;
  justify-content: center;
}

.about__image {
  width: 420px;
  height: 610px;
}

@media screen and (max-width: 1000px) {
  .about {
    padding: 30px;
  }

  .about__content {
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
  }

  .about__image-wrapper {
    margin-top: 40px;
  }

  .about__title {
    font-size: 70px;
  }
}

@media screen and (max-width: 468px) {
  .about__subtitle {
    font-size: 32px;
  }

  .about__image {
    width: 100%;
    height: 100%;
  }
}
</style>
