<template>
    <div>
        <header class="page-header">
            <button class="menu-toggle-button" @click="menuToggle">
                <i class="icon-hamburger"></i><span class="menu-toggle-label">Menu</span>
            </button>
        </header>
        <SiteMenu :is-visible="isVisible"/>
    </div>
</template>

<script>
export default {
  name: 'page-header',
  data() {
      return {
          isVisible: false,
      };
  },
  methods: {
      menuToggle() {
        this.isVisible = !this.isVisible;
      }
  }
};
</script>

<style lang="scss" scoped>
    .page-header {
        display: flex;
        justify-content: flex-end;
        background-color:#fff;
        padding: 1rem;
        width: 100%;
        position: fixed;
        top: 0;
        z-index: 999;
        box-shadow: 0px 3px 9px 2px rgb(0 0 0 / 25%);
        @media screen and (min-width: 1024px) {
            padding: 1rem 2rem;
        }
    }
    .menu-toggle {
        &-button {
            color: #000E54;
            background-color: transparent;
            font-weight: bold;
            font-size: 1.15rem;
            border: none;
            display: flex;
            align-items: center;
            & > i {
                font-size: 1.5rem;
                 @media screen and (min-width: 1024px) {
                     font-size: 1.15rem;
                 }
            }
            @media screen and (min-width: 1024px) {
                padding: .5rem 1.5rem;
                border: 2px solid #000E54;
            }
        }
        &-label {
            text-transform: uppercase;
            display: flex;
            width: 0;
            height: 0;
            overflow: hidden;
            @media screen and (min-width: 1024px){
                width: auto;
                height: auto;
                margin-left: 1rem;
            }
        }
    }
</style>