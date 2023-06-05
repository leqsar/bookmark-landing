<script setup>
import img1 from '../assets/images/logo-chrome.svg'
import img2 from '../assets/images/logo-firefox.svg'
import img3 from '../assets/images/logo-opera.svg'
</script>

<script>
    export default {
        data() {
            return {
                extensions: [
                    {
                        name: 'Chrome',
                        version: '62',
                        img: img1
                    },
                    {
                        name: 'Firefox',
                        version: '55',
                        img: img2
                    },
                    {
                        name: 'Opera',
                        version: '46',
                        img: img3
                    },
                ]
            }
        }
    }
</script>

<template>
    <section class="extensions-wrapper">
        <article class="extensions-main-info">
            <h2>Download the extension</h2>
            <p>
                We’ve got more browsers in the pipeline. Please do let us know if you’ve 
                got a favourite you’d like us to prioritize.
            </p>
        </article>
        <ul class="extensions">
                <li v-for="extension in extensions" class="extension-info">
                    <img :src="extension.img" alt="Web browser logo">
                    <h3>Add to {{ extension.name }}</h3>
                    <p>Minimum version {{ extension.version }}</p>
                    <button>Add & Install Extension</button>
                </li>
            </ul>
    </section>
</template>

<style scoped lang="sass">
    @import "../input.sass"

    .extensions-wrapper
        @include defaultSectionMargins
        width: 915px
        text-align: center

        .extensions-main-info
            p  
                @include pFontRule
                margin: 0 auto 
                width: 530px
                margin-top: $contentVerticalMargin

        .extensions
            margin-top: 60px
            width: 100%
            display: grid
            grid-template-areas: 'a . .' 'a b .' 'a b c' 'a b c' 'a b c' 'a b c' '. b c' '. . c'
            column-gap: 30px


            li  
                position: relative
                height: 360px
                box-shadow: 2px 2px 20px -10px $grayishBlue
                border-radius: 10px

                &:before
                    content: ''
                    position: absolute
                    top: 270px
                    left: 0
                    width: 100%
                    height: 4px
                    background-image: url(../assets/images/bg-dots.svg)

                img, h3
                    margin-top: 35px
                
                p
                    margin-top: 20px
                    color: $grayishBlue

                button
                    margin-top: 60px
                    width: $bigBttnWidth
                    height: $bttnHeight
                    background-color: $softBlue
                    color: white
                    font-weight: 600

                    &:hover
                        background-color: white
                        color: $softBlue 
                        border: 2px solid $softBlue

            li:nth-child(1)
                grid-area: a

            li:nth-child(2)
                grid-area: b

            li:nth-child(3)
                grid-area: c
            

</style>