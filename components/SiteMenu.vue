<template>
    <div class="site-menu-container" :class="showMenu">
        <div class="site-menu" :class="showMenu">
            <nav>
                <ul class="site-menu-list">
                <li class="site-menu-list-item">
                    Home
                    </li>
                    <li class="site-menu-list-item">
                    Icon, Index, Symbol
                    </li>
                    <li class="site-menu-list-item">
                    Ancient Egypt
                    </li>
                    <li class="site-menu-list-item">
                    The Digital Past and Present
                    </li>
                    <li class="site-menu-list-item">
                    The Future
                    </li>
                <li class="site-menu-list-item">
                    End Notes
                    </li>
                <li class="site-menu-list-item">
                    Bibliography
                    </li>
                </ul>
            </nav>
        </div>
        <div class="site-menu-overlay"></div>
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
    background: #fff;
    position: fixed;
    top: 0;
    z-index: 99;
    width: 0;
    box-shadow: 0px 3px 10px 3px rgb(0 0 0 / 25%);
    height: 100%;
    overflow: hidden;
    @media screen and (min-width: 1025px) {
        top: 0;
        right: 0;
        height: 100%;
        
    }
    &-container {
        display: none;
        position: absolute;
        top: 0;
        width: 100%;
        height: 100000000000000px;
        &.is-active {
            display: block;
        }
    }
    & nav {
        margin-top: 90px;
    }
    &-list {
        list-style-type: none;
        margin: 0;
        padding: 0;
        &-item {
            padding: .75rem 1rem;
            margin: 0;
            &:not(first-child) {
                border-bottom: 1px solid #dcdadb;
            }
        }
    }
    &-overlay {
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        background-color: rgba(0,0,0,.8);
        z-index: 9;
    }
    &.is-active {
        display: block;
        width: 100%;
        @media screen and (min-width: 1025px) {
            width: 300px;
        }
    }
}
</style>

