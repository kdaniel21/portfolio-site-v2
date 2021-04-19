<template>
  <div id="about">
    <!-- INTRODUCTION SECTION -->
    <h1>About me</h1>
    <p>
      Hi! My name is Daniel Kiss, an aspiring
      <span class="blue">full-stack developer</span> based in
      <span class="blue">Sopron</span>, Hungary 🇭🇺.
    </p>
    <p>
      I’m currently a high school student and I'm also working for a cool media
      startup called
      <a href="https://varia.media" target="_blank" class="varia-yellow">
        Varia Media
      </a>
      as junior developer.
    </p>
    <!-- TECHNOLOGIES SECTION -->
    <h2>Technologies I've worked with</h2>
    <techs :techs="techs"></techs>
    <div class="action">
      <nuxt-link to="projects">
        <div class="btn projects-btn">Take a look at my projects</div>
      </nuxt-link>
      <nuxt-link to="contact">
        <div class="btn">Contact Me</div>
      </nuxt-link>
    </div>
  </div>
</template>
<script>
export default {
  name: 'About',
  data() {
    return {
      techs: [
        {
          name: 'JavaScript',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1596170003/portfolio-site/tech-icons/javascript_oo047w.svg',
        },
        {
          name: 'TypeScript',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1596170003/portfolio-site/tech-icons/typescript_japrq8.svg',
        },
        {
          name: 'Angular',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1596170008/portfolio-site/tech-icons/angular_ut7ry9.svg',
        },
        {
          name: 'Vue',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1596170003/portfolio-site/tech-icons/vue_ovr6z9.svg',
        },
        {
          name: 'GraphQL',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1618832179/portfolio-site/tech-icons/graphql_jxutab.svg',
        },
        {
          name: 'Node.js',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1596170002/portfolio-site/tech-icons/nodejs_dolm0a.svg',
        },
        {
          name: 'Java',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1596170003/portfolio-site/tech-icons/java_azbwoq.svg',
        },
        {
          name: 'Git',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1596170005/portfolio-site/tech-icons/git_i4eslw.svg',
        },
        {
          name: 'MongoDB',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1596170003/portfolio-site/tech-icons/mongodb_jm7jrz.svg',
        },
        {
          name: 'PostgreSQL',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1618832351/portfolio-site/tech-icons/Postgresql_elephant_r4wfto.svg',
        },
        {
          name: 'Firebase',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1596170006/portfolio-site/tech-icons/firebase_hw3khm.svg',
        },
        {
          name: 'CSS',
          img:
            'https://res.cloudinary.com/kdaniel/image/upload/v1596170007/portfolio-site/tech-icons/css_gw5jlc.svg',
        },
      ],
    }
  },
}
</script>
<style scoped>
.varia-yellow {
  color: rgb(255, 192, 0);
}
#about {
  margin-left: 1rem;
  color: #2b2d42;
}
.action {
  display: flex;
  margin-top: 2rem;
  flex-wrap: wrap;
}

.projects-btn {
  margin-right: 1rem;
}
</style>
