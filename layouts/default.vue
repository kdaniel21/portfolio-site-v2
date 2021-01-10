<template>
  <div id="app">
    <div style="min-height: calc(100vh - 195px - 10px)">
      <header />
      <transition name="component-fade" mode="out-in">
        <Nuxt />
      </transition>
    </div>
    <cookie-consent />
    <footer />
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
