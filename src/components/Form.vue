<script setup>
</script>

<template>
    <section class="form-wrapper">
        <p>35,000+ already joined</p>
        <h2>Stay up-to-date with what we’re doing</h2>
        <form action="">
            <input type="email">
            <button>Contact Us</button>
        </form>
    </section>
</template>

<style scoped lang="sass">
    @import "../input.sass"

    .form-wrapper
        @include defaultSectionMargins
        width: 100%
        height: 360px
        display: flex
        flex-direction: column
        align-items: center
        background-color: $softBlue
        text-align: center
        padding-top: 70px
        box-sizing: border-box
        
        p, h2
            color: white !important

        p
            text-transform: uppercase
            letter-spacing: 2px

        h2 
            width: 410px
            margin-top: 50px

        form
            margin-top: $contentVerticalMargin

            input
                width: 300px
                height: 45px
                padding: 15px
                box-sizing: border-box
                font-size: 16px
                border-radius: 5px
                border: 0

                &:focus
                    outline: 0

            button
                width: $smallBttnWidth
                height: $bttnHeight
                margin-left: 20px
                background-color: $softRed
                color: white

                &:hover
                    background-color: white
                    color: $softRed
                    border: 2px solid $softRed

</style>