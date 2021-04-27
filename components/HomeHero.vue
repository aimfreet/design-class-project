<template>
    <div class="home-hero">
        <div class="home-hero__image" />
        <div class="home-hero__overlay" />
        <div class="home-hero__content">
            <h1 class="home-hero__heading">Icons &amp; Emojis <br> The New Hieroglyphics</h1>
            <p class="home-hero__copy">What can ancient hieroglyphics tell us about the future of our communication?</p>
            <p class="margin-top-4 font-size-9">Written by Aimee Maroney</p>
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
        height: 100vh;
        position: absolute;
        top: 0;
        @media screen and (min-width: 1024px) {
            justify-content: center;
        }
        &__heading {
            @media screen and (min-width: 1024px) {
                font-size: 72px;
                line-height: 84px;
            }
        }
        &__copy {
            @media screen and (min-width: 1024px) {
                font-size: 28px;
                line-height: 36px;
                font-weight: bold;
            }
        }
        &__image {
            width: 100%;
            height: 100%;
            background-image: url('https://tankgirl-storage.s3.amazonaws.com/codepen-images/IconBanner-blue.svg');
            background-repeat: no-repeat;
            background-color: #000;
            background-size: cover;
            background-position: center center;
            position: absolute;
            top: 0;
            z-index: 0;
        }
        &__overlay {
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,.45);
            position: absolute;
            top: 5;
            z-index: 0;
        }
        &__content {
            display: flex;
            flex-direction: column;
            position: relative;
            top: 9;
            padding: 1.5rem;
            margin-top: 100px;
            color: #fff;
            margin-left: 1.5rem;
            margin-right: 1.5rem;
            text-shadow: 0.1rem 0.1rem 0 rgb(0 0 0 / 15%), 0.1rem -0.1rem 0 rgb(0 0 0 / 15%), -0.1rem 0.1rem 0 rgb(0 0 0 / 15%), -0.1rem -0.1rem 0 rgb(0 0 0 / 15%);
            @media screen and (min-width: 1024px){
                max-width: 50%;
                margin-left: 2rem;
                padding: 3rem;
            }
        }
    }
</style>