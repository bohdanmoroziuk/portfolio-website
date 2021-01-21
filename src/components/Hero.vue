<template>
  <section class="hero section">
    <div class="hero__content">
      <div class="hero__column hero__column--left">
        <span class="hero__user">{{ user }}</span>
        <h1 class="hero__title">{{ title }}</h1>
        <p class="hero__description">{{ description }}</p>
      </div>
      <div class="hero__column hero__column--right">
        <img class="hero__image" src="/images/ai-brain.svg" alt="brain">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Hero',
  props: {
    user: {
      type: String,
      required: true,
    },
    title: {
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
.hero {
  background: #002ed0;
  padding: 0 60px;
  color: #fff;
}

.hero__content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 820px;
}

.hero__column--left {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-start;
}

.hero__title {
  font-size: 90px;
}

.hero__description {
  font-size: 16px;
  line-height: 2.4;
}

.hero__column--right {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.hero__image {
  width: 100%;
  height: 100%;
}

@media screen and (max-width: 1100px) {
  .hero {
    padding: 30px;
  }

  .hero__content {
    grid-template-columns: 1fr;
  }

  .hero__title {
    font-size: 80px;
  }
}

@media screen and (max-width: 468px) {
  .hero__content {
    grid-template-rows: 600px;
  }

  .hero__title {
    font-size: 32px;
  }
}
</style>
