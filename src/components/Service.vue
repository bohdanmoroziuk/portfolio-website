<template>
  <div class="service">
    <img class="service__icon" :src="icon" alt="service icon">
    <div class="service__content">
      <h3 class="service__title">{{ title }}</h3>
      <p class="service__description">{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Service',
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      default: '',
    },
    icon: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.service {
  display: flex;
  align-items: flex-start;
}

.service__icon {
  margin-right: 50px;
}

.service__title {
  font-size: 16px;
  text-transform: uppercase;
  margin-bottom: 16px;
}

.service__description {
  line-height: 2;
}

@media screen and (max-width: 468px) {
  .service {
    margin-top: 40px;
  }

  .service__icon {
    margin-right: 16px;
  }
}
</style>
