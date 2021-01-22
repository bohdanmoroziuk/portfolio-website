<template>
  <section class="portfolio section">
    <div class="portfolio__container">
      <h2 class="portfolio__title">{{ title }}</h2>
      <div class="portfolio__content">
        <div class="portfolio__left">
          <img class="portfolio__image" src="/images/portfolio-4.svg" alt="dashboard">
        </div>
        <div class="portfolio__right">
          <h3>Web Design Company</h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Facilis, ducimus dicta, laudantium eos repellendus ipsum
            magni modi minus impedit aliquam asperiores rerum velit id
            saepe beatae ab, perferendis doloribus amet?
          </p>
          <router-link to="/">See more</router-link>
        </div>
      </div>
      <div class="portfolio__projects">
        <img
          class="portfolio__project-image"
          v-for="project of projects"
          :key="project.name"
          :src="project.image.src"
          :alt="project.image.alt"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Portfolio',
  props: {
    title: {
      type: String,
      default: 'Portfolio',
    },
    projects: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.portfolio {
  background: #002ed0;
  color: #fff;
}

.portfolio__container {
  padding: 100px 0 100px 60px;
}

.portfolio__title {
  font-size: 110px;
  color: #fff;
  -webkit-text-fill-color: transparent;
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: #fff;
  margin-bottom: 32px;
}

.portfolio__content {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.portfolio__image {
  height: 100%;
  width: 100%;
}

.portfolio__right {
  padding: 150px 100px 0 20px;
}

.portfolio__right h2 {
  margin-bottom: 40px;
  font-size: 30px;
}

.portfolio__right p {
  margin-bottom: 50px;
  line-height: 2.5;
}

.portfolio__right a {
  color: #fff;
  text-decoration: none;
}

.portfolio__projects {
  display: flex;
  justify-content: center;
  padding: 32px 64px;
}

.portfolio__project-image {
  padding: 0 8px;
  width: 100%;
  height: 100%;
}

@media screen and (max-width: 1368px) {
  .portfolio__projects {
    flex-direction: column;
  }
}

@media screen and (max-width: 1000px) {
  .portfolio {
    padding: 30px;
  }

  .portfolio__title {
    font-size: 70px;
  }

  .portfolio__content {
    grid-template-columns: 1fr;
  }

  .portfolio__container {
    padding-left: 0;
  }

  .portfolio__right {
    margin-bottom: 60px;
  }
}

@media screen and (max-width: 468px) {
  .portfolio {
    padding: 10px;
  }

  .portfolio__title {
    font-size: 40px;
  }
}
</style>
