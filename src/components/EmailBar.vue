<template>
  <div class="email-bar">
    <img class="email-bar__image" :src="image.src" :alt="image.alt">
    <h4 class="email-bar__title">{{ title }}</h4>
    <span class="email-bar__address">{{ email }}</span>
  </div>
</template>

<script>
import { isEmail } from '@/validators';

export default {
  name: 'EmailBar',
  props: {
    title: {
      type: String,
      default: 'Email',
    },
    email: {
      type: String,
      required: true,
      validator: isEmail,
    },
    image: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.email-bar {
  position: absolute;
  background: yellow;
  height: 80px;
  bottom: -40px;
  right: 0;
  width: 80%;
  color: #000;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.email-bar__image {
  margin: 0 40px;
}

.email-bar__title {
  margin-right: 40px;
  font-weight: 700;
  text-transform: uppercase;
}

@media screen and (max-width: 768px) {
  .email-bar {
    width: 100%;
  }
}

@media screen and (max-width: 468px) {
  .email-bar__image {
    margin: 0 20px;
  }

  .email-bar__title {
    margin-right: 20px;
  }
}
</style>
