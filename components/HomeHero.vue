<template>
    <div class="home-hero">
        <div class="home-hero__image" />
        <div class="home-hero__overlay" />
        <div class="home-hero__content">
            <h1>Lorem Ipsum Dolor Amet</h1>
            <p> Nulla aliquet enim tortor at auctor urna nunc id cursus.
            Tellus pellentesque eu tincidunt tortor aliquam nulla. Porta non pulvinar neque laoreet suspendisse.</p>
            <p class="margin-top-4">Written by Aimee Maroney</p>
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
        height: 90vh;
        position: absolute;
        top: 0;
        @media screen and (min-width: 1024px) {
            justify-content: center;
        }
        &__image {
            width: 100%;
            height: 100%;
            background-image: url('https://tankgirl-storage.s3.amazonaws.com/codepen-images/IconBanner.svg');
            background-repeat: no-repeat;
            background-size: cover;
            background-position: center center;
            position: absolute;
            top: 0;
            z-index: 0;
        }
        &__overlay {
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,.1);
            position: absolute;
            top: 5;
            z-index: 0;
        }
        &__content {
            display: flex;
            flex-direction: column;
            position: relative;
            top: 9;
            padding: 3rem;
            margin-top: 100px;
            background: rgba(255,255,255,.9);
            margin-left: 1rem;
            margin-right: 1rem;
            @media screen and (min-width: 1024px){
                max-width: 50%;
                margin-left: 2rem;
            }
        }
    }
</style>