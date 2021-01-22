<template>
  <footer class="footer section">
    <div class="footer__container">
      <div class="footer__info">
        <h2 class="footer__author">{{ author }}</h2>
        <p class="footer__text">{{ text }}</p>
      </div>
      <nav class="footer__nav">
        <router-link
          class="footer__nav-link"
          v-for="link of nav"
          :key="link.name"
          :to="link.to"
        >
          {{ link.name }}
        </router-link>
      </nav>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    author: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
    nav: {
      type: Array,
      requried: true,
    },
  },
};
</script>

<style scoped>
.footer {
  background: #002ed0;
  color: #fff;
}

.footer__container {
  padding: 60px;
  display: grid;
  grid-template-columns: 1fr 2fr;
}

.footer__info {
  display: flex;
  flex-direction: column;
}

.footer__author {
  margin-bottom: 24px;
}

.footer__text {
  line-height: 2;
}

.footer__nav {
  display: flex;
  justify-content: space-between;
  padding: 0 100px;
}

.footer__nav-link {
  color: #fff;
  text-decoration: none;
  text-transform: uppercase;
  font-weight: 700;
}

@media screen and (max-width: 1000px) {
  .footer__container {
    padding: 60px 24px;
    grid-template-columns: 1fr 1fr;
  }

  .footer__nav {
    flex-direction: column;
  }
}

@media screen and (max-width: 468px) {
  .footer__nav {
    padding: 0 16px;
  }
}
</style>
