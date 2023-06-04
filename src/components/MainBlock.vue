<script setup></script>

<script></script>

<template>
  <section class="main-block">
    <article class="main-info-wrapper">
      <h1 class="main-info-heading">A Simple Bookmark Manager</h1>
      <p>
        A clean and simple interface to organize your favourite websites. Open a
        new browser tab and see your sites load instantly. Try it for free.
      </p>
      <div class="buttons-wrapper">
        <button>Get it on Chrome</button>
        <button>Get it on Firebox</button>
      </div>
    </article>
    <div class="image-wrapper">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        width="536"
        height="346"
      >
        <defs><rect id="a" width="536" height="346" rx="8" /></defs>
        <g fill="none" fill-rule="evenodd">
          <mask id="b" fill="#fff"><use xlink:href="#a" /></mask>
          <use fill="#E8EAF6" fill-rule="nonzero" xlink:href="#a" />
          <g mask="url(#b)">
            <path fill="#5368df" d="M-3.53.197h547v59h-547z" />
            <g transform="translate(22.47 14.197)" fill="#FFF">
              <circle cx="16" cy="16" r="16" opacity=".245" />
              <circle cx="477" cy="16" r="16" opacity=".104" />
              <g transform="translate(47 6)">
                <rect width="120" height="6" opacity=".75" rx="3" />
                <rect width="64" height="6" y="14" opacity=".25" rx="3" />
              </g>
            </g>
          </g>
          <g mask="url(#b)">
            <g transform="translate(57 93)">
              <rect width="261" height="316" fill="#FFF" rx="8" />
              <rect width="128" height="316" x="295" fill="#FFF" rx="8" />
              <rect
                width="120"
                height="6"
                x="78.47"
                y="38.197"
                fill="#242A45"
                opacity=".5"
                rx="3"
              />
            </g>
          </g>
          <g transform="translate(88.47 115.197)">
            <circle cx="16" cy="26" r="16" fill="#F98E5D" />
            <rect
              width="88"
              height="6"
              x="284"
              fill="#242A45"
              opacity=".25"
              rx="3"
            />
            <rect
              width="88"
              height="6"
              x="284"
              y="20"
              fill="#242A45"
              opacity=".25"
              rx="3"
            />
            <rect
              width="88"
              height="6"
              x="284"
              y="40"
              fill="#242A45"
              opacity=".25"
              rx="3"
            />
            <rect
              width="88"
              height="6"
              x="284"
              y="60"
              fill="#242A45"
              opacity=".25"
              rx="3"
            />
            <rect
              width="88"
              height="6"
              x="284"
              y="94"
              fill="#242A45"
              opacity=".25"
              rx="3"
            />
            <rect
              width="88"
              height="6"
              x="284"
              y="114"
              fill="#242A45"
              opacity=".25"
              rx="3"
            />
            <rect
              width="88"
              height="6"
              x="284"
              y="134"
              fill="#242A45"
              opacity=".25"
              rx="3"
            />
            <rect
              width="64"
              height="6"
              x="47"
              y="30"
              fill="#242A45"
              opacity=".25"
              rx="3"
            />
          </g>
          <g transform="translate(88.47 181.197)">
            <circle cx="16" cy="16" r="16" fill="#6AC6D6" />
            <rect
              width="120"
              height="6"
              x="47"
              y="6"
              fill="#242A45"
              opacity=".5"
              rx="3"
            />
            <rect
              width="64"
              height="6"
              x="47"
              y="20"
              fill="#242A45"
              opacity=".25"
              rx="3"
            />
          </g>
          <g transform="translate(88.47 237.197)">
            <circle cx="16" cy="16" r="16" fill="#A47ED4" />
            <rect
              width="120"
              height="6"
              x="47"
              y="6"
              fill="#242A45"
              opacity=".5"
              rx="3"
            />
            <rect
              width="64"
              height="6"
              x="47"
              y="20"
              fill="#242A45"
              opacity=".25"
              rx="3"
            />
          </g>
          <g transform="translate(88.47 293.197)">
            <circle cx="16" cy="16" r="16" fill="#EC7878" />
            <rect
              width="120"
              height="6"
              x="47"
              y="6"
              fill="#242A45"
              opacity=".5"
              rx="3"
            />
            <rect
              width="64"
              height="6"
              x="47"
              y="20"
              fill="#5368df"
              opacity=".25"
              rx="3"
            />
          </g>
        </g>
      </svg>
    </div>
    <div class="blue-box"></div>
  </section>
</template>

<style lang="sass" scoped>
@import "../input.sass"

.main-block
  position: relative
  width: 100%
  padding-left: $bodyMarginLeft
  box-sizing: border-box
  display: flex

  .main-info-wrapper
      display: flex
      flex-direction: column
      width: 470px

      .main-info-heading
          margin-top: 145px
          font-size: $h1FontSize
          color: $veryDarkBlue
          letter-spacing: 1px
          font-weight: 500
          line-height: 40px

      p
          margin-top: $contentVerticalMargin
          font-size: $mainFontSize
          color: $grayishBlue
          width: 100%

      .buttons-wrapper
          margin-top: $contentVerticalMargin

          button
              width: $mediumBttnWidth
              height: $bttnHeight
              color: $grayishBlue
              font-size: $bttnFotnSize
              font-weight: 600
              border: 2px solid $grayishBlue
              background-color: white
              border-radius: 5px

              &:hover
                  cursor: pointer
                  color: $softBlue
                  border: 2px solid $softBlue

              &:last-of-type
                  margin-left: 20px

  .image-wrapper
      margin-left: 125px
      margin-top: 70px
      width: 578px
      height: 384px
      padding: 20px
      box-sizing: border-box
      border-radius: 20px
      background: linear-gradient(145deg, rgba(60,60,60,1) 0%, rgba(0,0,0,1) 60%)

  .blue-box
      position: absolute
      right: 0
      top: 200px
      width: 500px
      height: 350px
      border-top-left-radius: 175px
      border-bottom-left-radius: 175px
      background-color: $softBlue
      z-index: -1
</style>
