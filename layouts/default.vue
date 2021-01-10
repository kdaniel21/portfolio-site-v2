<template>
  <div id="default">
    <the-header />
    <div id="content">
      <transition name="component-fade" mode="out-in">
        <Nuxt />
      </transition>
    </div>
    <the-footer />
    <cookie-consent />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Daniel Kiss',
    }
  },
}
</script>

<style scoped>
#default {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
#content {
  padding-top: 60px;
  flex-grow: 1;
}
</style>
