<script setup>
import img1 from '../assets/images/illustration-features-tab-1.svg'
import img2 from '../assets/images/illustration-features-tab-2.svg'
import img3 from '../assets/images/illustration-features-tab-3.svg'
</script>

<script>
    export default {
        props: ['heading', 'mainContent'],
        methods: {
            chooseImg(heading) {
                if(heading==='Bookmark in one click') {
                    return {
                        src: img1,
                        ratio: '268 / 173'
                    }
                } else if(heading==='Intelligent search') {
                    return {
                        src: img2,
                        ratio: '22 / 19'
                    }
                } else if(heading==='Share your bookmarks') {
                    return {
                        src: img3,
                        ratio: '22 / 19'
                    }
                }
            }
        }
    }
</script>

<template>
    <section class="feature-wrapper">
        <img :src="this.chooseImg(heading).src" alt="" class="feature-img" :style="{aspectRatio: this.chooseImg(heading).ratio}">
        <div class="blue-box"></div>
        <article class="feature-main-info">
            <h2 class="feature-heading">{{heading}}</h2>
            <p class="feature-content">{{mainContent}}</p>
            <button>More info</button>
        </article>
    </section>
</template>

<style scoped lang="sass">
    @import "../input.sass"

    .feature-wrapper
        position: relative
        width: 100%
        padding-left: $bodyMarginLeft
        box-sizing: border-box
        display: flex

        @media screen and (max-width: $mobileWidth)
            padding-left: 4%
            flex-direction: column

        .feature-main-info
            display: flex
            flex-direction: column
            width: 440px
            margin-top: 130px
            margin-left: 125px

            @media screen and (max-width: $mobileWidth)
                width: 100%
                margin: 0 auto
                margin-top: $contentVerticalMargin

            .feature-heading
                text-align: left

                @media screen and (max-width: $mobileWidth)
                    text-align: center

            .feature-content
                color: $grayishBlue
                font-size: $mainFontSize
                text-align: left
                margin-top: $contentVerticalMargin

                @media screen and (max-width: $mobileWidth)
                    margin-top: $contentVerticalMargin/2
                    text-align: center
            
            button
                margin-top: $contentVerticalMargin
                width: $smallBttnWidth
                height: $bttnHeight
                background-color: $softBlue
                color: white

                @media screen and (max-width: $mobileWidth)
                    margin: 0 auto
                    margin-top: $contentVerticalMargin/2
    
        .blue-box
            left: 0
            top: 150px
            border-top-right-radius: 175px
            border-bottom-right-radius: 175px

            @media screen and (max-width: $mobileWidth)
                top: 70px
                border-top-right-radius: 140px
                border-bottom-right-radius: 140px

        .feature-img 
            margin-top: 75px
            width: 537px

            @media screen and (max-width: $mobileWidth)
                margin: 0 auto
                margin-top: 45px
                width: 275px

</style>