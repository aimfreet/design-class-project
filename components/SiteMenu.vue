<template>
    <div class="site-menu-container" :class="showMenu">
        <div class="site-menu" :class="showMenu">
            <nav>
                <ul class="site-menu-list">
                    <li class="site-menu-list-item">
                        <a href="#"
                        class="site-menu-link"
                        v-scroll-to="{
                        el: '#home',
                        force: true,
                        cancelable: false,
                        onDone: scrollDone
                        }">
                            Home
                        </a>
                    </li>
                    <li class="site-menu-list-item">
                        <a href="#" 
                        class="site-menu-link"
                        v-scroll-to="{
                        el: '#icon-index-symbol',
                        force: true,
                        cancelable: false,
                        onDone: scrollDone
                        }">
                            Icon, Index, Symbol
                        </a>
                    </li>
                    <li class="site-menu-list-item">
                        <a href="#" 
                        class="site-menu-link"
                        v-scroll-to="{
                        el: '#ancient-egypt',
                        force: true,
                        cancelable: false,
                        onDone: scrollDone
                        }">
                            Ancient Egypt
                        </a>
                    </li>
                    <li class="site-menu-list-item">
                        <a href="#" 
                        class="site-menu-link"
                        v-scroll-to="{
                        el: '#digital-past-present',
                        force: true,
                        cancelable: false,
                        onDone: scrollDone
                        }">
                            The Digital Past and Present
                        </a>
                    </li>
                    <li class="site-menu-list-item">
                        <a href="#" 
                        class="site-menu-link"
                        v-scroll-to="{
                        el: '#the-future',
                        force: true,
                        cancelable: false,
                        onDone: scrollDone
                        }">
                            The Future
                        </a>
                    </li>
                    <li class="site-menu-list-item">
                        <a href="#" class="site-menu-link"
                        v-scroll-to="{
                        el: '#end-notes',
                        force: true,
                        cancelable: false,
                        onDone: scrollDone
                        }">
                            End Notes
                        </a>
                    </li>
                    <li class="site-menu-list-item">
                        <a href="#" class="site-menu-link"
                        v-scroll-to="{
                        el: '#bibliography',
                        force: true,
                        cancelable: false,
                        onDone: scrollDone
                        }">
                            Bibliography
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
        <div class="site-menu-overlay" @click="closeMenu"></div>
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
    methods:{
        closeMenu() {
            this.isVisible = !this.isVisible;
        },
    },
    mounted () {
        const closeBar = document.querySelector('.site-menu-link');
        closeBar.addEventListener('click', this.closeMenu);
    },
    beforeDestroy () {
        document.removeEventListener('click',this.close)
    }
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
            & > a {
                font-weight: normal;
                text-decoration: none;
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

