<script setup></script>

<script>
export default {
    data() {
        return {
            email: '',
            error: false
        }
    },
    methods: {
        validateForm() {
            const mailFormat = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
            if (this.email.match(mailFormat)) {
                this.error = false
            } else {
                this.error = true;
            }
        },
    }
}
</script>

<template>
  <section class="form-wrapper">
    <p>35,000+ already joined</p>
    <h2>Stay up-to-date with what we’re doing</h2>
    <form  v-on:submit.prevent="onSubmit">
      <input type="text" v-model="email" :class="{error:error}"/>
      <button @click="validateForm">Contact Us</button>
    </form>
    <p class="error-wrapper" v-show="error">Whoops, make sure it's an email</p>
  </section>
</template>

<style scoped lang="sass">
@import "../input.sass"

.form-wrapper
    @include defaultSectionMargins
    position: relative
    width: 100%
    height: 360px
    display: flex
    flex-direction: column
    align-items: center
    background-color: $softBlue
    text-align: center
    padding-top: 70px
    box-sizing: border-box

    @media screen and (max-width: $mobileWidth)
        margin-top: 90px

    p
        text-transform: uppercase
        letter-spacing: 3px
        font-weight: 500

        @media screen and (max-width: $mobileWidth)
            font-size: 12px          

    h2
        width: 410px
        margin-top: 50px
        
        @media screen and (max-width: $mobileWidth)
            margin-top: $contentVerticalMargin/2

    p, h2
        color: white !important
       
        @media screen and (max-width: $mobileWidth)
           width: 90%

    form
        margin-top: $contentVerticalMargin

        @media screen and (max-width: $mobileWidth)
            width: 90%
            display: flex
            flex-direction: column
            gap:  $contentVerticalMargin

        input
            position: relative
            width: 300px
            height: 45px
            padding: 15px
            box-sizing: border-box
            font-size: 16px
            border-radius: 5px
            border: 0

            @media screen and (max-width: $mobileWidth)
                width: 100%

            &:focus
                outline: 0

        .error 
            position: relative
            border: 2px solid $softRed
            border-bottom-left-radius: 0
            border-bottom-right-radius: 0
            

        button
            width: $smallBttnWidth
            height: $bttnHeight
            margin-left: 20px
            background-color: $softRed
            color: white

            @media screen and (max-width: $mobileWidth)
                width: 100%
                margin-left: 0 

            &:hover
                background-color: white
                color: $softRed
                border: 2px solid $softRed

    .error-wrapper
        position: absolute
        top: 275px
        left: 502.5px
        width: 300px
        height: 25px
        padding-top: 5px
        padding-left: 10px
        background-color: $softRed
        border: 2px solid $softRed
        border-bottom-left-radius: 5px
        border-bottom-right-radius: 5px
        color: white
        font-size: 10px
        box-sizing: border-box
        text-align: left

        @media screen and (max-width: $mobileWidth)
            left: 5%
            top: 240px
            width: 338px

</style>
