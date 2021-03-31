<template>
    <div class="site-menu">
        <nav>
            <ul class="site-menu-list">
               <li class="site-menu-list-item">Home</li>
               <li class="site-menu-list-item">Timeline</li>
               <li class="site-menu-list-item">Bibliography</li>
            </ul>
        </nav>
    </div>
</template>

<style lang="scss" scoped>
.site-menu {
    background: #fff;
    position: fixed;
    z-index: 999999;
    top: 90px;
    right: 0;
    margin-right: 1rem;
    &-list {
        list-style-type: none;
        margin: 0;
        padding: 0;
        &-item {
            padding: .5rem 1rem;
            border-top: 1px solid #dcdadb;
            margin: 0;
        }
    }
}
</style>

