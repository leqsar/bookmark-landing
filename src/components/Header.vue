<script setup>
</script>

<script>
</script>

<template>
  <header class="header">
    <img class="logo" src="../assets/images/logo-bookmark.svg" alt="Company logo">
    <nav class="header-navigation-wrapper">
      <ul class="header-navigation">
        <li>feature</li>
        <li>pricing</li>
        <li>contact</li>
      </ul>
    </nav>
    <button class="login-button">login</button>
  </header>
</template>

<style lang="sass" scoped >
  @import "../input.sass"

  .header
    height: 136px
    margin-left: $bodyMarginLeft
    display: flex
    align-items: center

    .header-navigation
      display: flex
      margin-left: 505px
      width: 295px
      justify-content: space-between

      li
        text-transform: uppercase
        font-size: 16px
        letter-spacing: 1px
        color: $veryDarkBlue

        &:hover
          cursor: pointer
          color: $softRed
    
    .login-button
      width: $smallBttnWidth
      height: $bttnHeight
      margin-left: 50px
      text-transform: uppercase
      background-color: $softRed
      color: white
      letter-spacing: 1px
      border-radius: 5px
      font-weight: 500

      &:hover
        border: 2px solid $softRed
        background-color: white
        color: $softRed
        cursor: pointer

</style>
