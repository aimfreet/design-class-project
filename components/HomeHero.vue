<template>
    <div class="home-hero">
        <div class="home-hero__content text-white text-shadow">
            <h1>Lorem Ipsum Dolor Amet</h1>
            <p> Nulla aliquet enim tortor at auctor urna nunc id cursus.
            Tellus pellentesque eu tincidunt tortor aliquam nulla. Porta non pulvinar neque laoreet suspendisse.</p>
            <p class="margin-top-auto">Written by Aimee Maroney</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .home-hero {
        background-color: #8D9299;
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 100%;
        height: 75vh;
        position: absolute;
        padding: 3rem;
        top: 0;
        &__content {
            display: flex;
            flex-direction: column;
            @media screen and (min-width: 1024px){
                max-width: 50%;
                height: 400px;
            }
        }
    }
</style>