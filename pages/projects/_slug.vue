<template>
  <div id="project-details">
    <transition
      appear
      appear-class="load-project"
      appear-active-class="load-project-active"
    >
      <div v-if="project" class="project">
        <img
          :src="project.img"
          alt="Project image"
          :title="project.name"
          class="project-image"
        />
        <h2>{{ project.name }}</h2>
        <p class="project-description">
          {{ project.description }}
        </p>
        <h2>Technologies Used</h2>
        <techs :techs="project.technologies"></techs>
        <div class="actions">
          <div class="date">Created: {{ project.created }}</div>
          <div class="buttons">
            <a v-if="project.repoUrl" :href="project.repoUrl" target="_blank">
              <div class="btn repo-btn">Repository</div>
            </a>
            <a v-if="project.demoUrl" :href="project.demoUrl" target="_blank">
              <div class="btn">Demo</div>
            </a>
          </div>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'ProjectDetails',
  async asyncData({ $content, params }) {
    const { slug } = params
    const project = await $content('projects').where({ slug }).fetch()

    return { project: project[0] }
  },
}
</script>

<style scoped>
.project {
  border-radius: 15px;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  width: 80%;
  margin: auto;
  margin-top: 5rem;
  padding: 1rem;
}
h2 {
  font-size: clamp(20px, 12vw, 55px);
}
.project-image {
  width: 100%;
}
.project-description {
  width: 100%;
}
.actions {
  display: flex;
  justify-content: space-between;
}
.buttons {
  display: flex;
  justify-content: space-between;
  width: min(16rem, 40vw);
}
.date {
  font-size: 20px;
  margin-top: auto;
  margin-left: 0.5rem;
  font-family: Kanit;
}

.load-project-active {
  transition: all 0.5s ease-in;
}
.load-project {
  opacity: 0;
}

@media only screen and (max-width: 800px) {
  .actions {
    flex-direction: column;
  }
  .buttons {
    margin-top: 0.8rem;
    justify-content: flex-end;
    width: 100%;
  }
  .btn {
    font-size: 18px;
    margin-right: 0.5rem;
  }
}
</style>
