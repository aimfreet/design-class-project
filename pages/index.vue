<template>
    <div class="home-page">
      <HomeHero />
      <div class="container-lg">
        <div class="home-page__content shadow-depth-1">
          <nuxt-content :document="page" />
        </div>
      </div>
    </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const page = await $content('home').fetch()

    return {
      page
    }
  }
}
</script>

<style lang="scss" scoped>
.home-page {
  &__content {
    position: relative;
    background-color: #fff;
    padding: 1.5rem;
    margin-top: calc(75vh - 150px);
  }
}
</style>
