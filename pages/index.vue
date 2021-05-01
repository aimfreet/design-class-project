<template>
    <div class="home-page">
      <HomeHero />
      <div class="container-xl">
        <div class="home-page__content page-text shadow-depth-1">
          <nuxt-content :document="page" />
          <EndNotes />
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
    margin-top: calc(90vh);
    @media screen and (min-width: 1024px) {
      margin-top: calc(100vh - 100px);
      padding: 3.5rem 2.5rem;
    }
  }
}
</style>
