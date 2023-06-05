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
                    return img1
                } else if(heading==='Intelligent search') {
                    return img2
                } else if(heading==='Share your bookmarks') {
                    return img3
                }
            }
        }
    }
</script>

<template>
    <section class="feature-wrapper">
        <img :src="this.chooseImg(heading)" alt="" class="feature-img">
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

        .feature-main-info
            display: flex
            flex-direction: column
            width: 440px
            margin-top: 130px
            margin-left: 125px

            .feature-heading
                text-align: left

            .feature-content
                color: $grayishBlue
                font-size: $mainFontSize
                text-align: left
                margin-top: $contentVerticalMargin
            
            button
                margin-top: $contentVerticalMargin
                width: $smallBttnWidth
                height: $bttnHeight
                background-color: $softBlue
                color: white
    
        .blue-box
            left: 0
            top: 150px
            border-top-right-radius: 175px
            border-bottom-right-radius: 175px

        .feature-img 
            margin-top: 75px
            width: 537px

</style>