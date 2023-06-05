<script setup>
</script>

<script>
    export default {
        data() {
            return {
                open: false,
                lineDisplay: 'block',
                arrowTransform: 'rotate(225deg)',
                color: 'hsl(231, 69%, 60%)'
            }
        },
        props: ['question', 'answer'],
        methods: {
            showAnswer() {
                this.open = !this.open;
                this.lineDisplay = this.lineDisplay==='none' ? 'block' : 'none'
                this.arrowTransform = this.arrowTransform==='rotate(225deg)' ? 'rotate(45deg)' : 'rotate(225deg)'
                this.color = this.color==='hsl(231, 69%, 60%)' ? 'hsl(0, 94%, 66%)' : 'hsl(231, 69%, 60%)'
            }
        }
    }
</script>

<template>
    <li>
        <h4 class="question" @click="showAnswer">{{ question }}</h4>
        <p class="answer" v-show="open">{{ answer }}</p>
        <div class="arrowhehe" @click="showAnswer"></div>
    </li>
</template>

<style scoped lang="sass">
    @import "../input.sass"

    li
        position: relative
        .question
            position: relative
            display: flex
            align-items: center
            width: 100%
            height: 60px
            font:
                weight: 400
                size: $mainFontSize
            letter-spacing: 0.5px
            user-select: none

            &:after
                content: ''
                position: absolute
                display: v-bind(lineDisplay)
                top: 60px
                width: 100%
                border-top: 1px solid $grayishBlue

            &:hover
                cursor: pointer
                color: $softRed

        .answer
            color: $grayishBlue
            font-size: 17px
            line-height: 30px

        img
            position: absolute
            right: 10px
            top: 30px
            transition: all 0.5s
            transform: v-bind(arrowTransform)

            

        .arrowhehe 
            position: absolute
            right: 10px
            top: 20px
            width: 10px
            height: 10px
            border-top: 3px solid v-bind(color)
            border-left: 3px solid v-bind(color)
            transition: all 0.5s
            transform: v-bind(arrowTransform)

            &:hover
                cursor: pointer

</style>