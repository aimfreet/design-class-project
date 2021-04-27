<template>
    <div class="site-menu" :class="showMenu">
        <nav>
            <ul class="site-menu-list">
               <li class="site-menu-list-item">
                   Home
                </li>
               <li class="site-menu-list-item">
                   Timeline
                </li>
               <li class="site-menu-list-item">
                   Bibliography
                </li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'site-menu',
    props: {
        isVisible: {
            type: String,
        },
    },
    computed: {
        showMenu() {
            return {
                'is-active': this.isVisible === true,
            };
        }
    },
};
</script>

<style lang="scss" scoped>
.site-menu {
    display: none;
    background: #fff;
    position: fixed;
    top: 57px;
    z-index: 99;
    width: 100%;
    box-shadow: 0px 3px 10px 3px rgb(0 0 0 / 25%);
    height: 100%;
    @media screen and (min-width: 1025px) {
        width: auto;
        top: 90px;
        right: 0;
        margin-right: 2rem;
        height: auto;
    }
    &-list {
        list-style-type: none;
        margin: 0;
        padding: 0;
        &-item {
            padding: .75rem 1rem;
            border-top: 1px solid #dcdadb;
            margin: 0;
        }
    }
    &.is-active {
        display: block;
    }
}
</style>

