<script setup>
import { questions } from "./constants";
import Question from "./Question.vue";
</script>

<script>
</script>

<template>
  <section class="faq-wrapper">
    <article class="faq-main-info">
      <h2>Frequently Asked Questions</h2>
      <p>
        Here are some of our FAQs. If you have any other questions you’d like
        answered please feel free to email us.
      </p>
    </article>
    <ul class="questions-wrapper">
        <Question 
            v-for="question in questions" 
            :question="question.question" 
            :answer="question.answer"
        />
    </ul>
    <button>More Info</button>
  </section>
</template>

<style scoped lang="sass">
    @import "../input.sass"

    .faq-wrapper
        @include defaultSectionMargins
        width: 536px
        
        .faq-main-info
            text-align: center

            p
                @include pFontRule
                margin-top: $contentVerticalMargin

        .questions-wrapper
            display: flex
            flex-direction: column
            width: 100%
            margin-top: 60px

        button 
            width: $smallBttnWidth
            height: $bttnHeight
            margin-top: 55px
            margin-left: 212px
            background-color: $softBlue
            color: white
            font-weight: 500

</style>
