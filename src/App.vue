<template>
  <div id="app">
    <div id="menu-view">
    <div id="name"> <img src="@/assets/logo.svg" alt="Logo"> </div>
      <div id="menu">
        <a class="social" href="https://twitter.com/_wost"> <feather type="twitter" /> </a>
        <a class="social _" href="https://www.linkedin.com/in/william-slettvold-%C3%B8stensen-303a56a1/"> <feather type="linkedin" /> </a>
        <a class="social _" href="https://github.com/wislos"> <feather type="github" /> </a>
      </div>
      <ul id="link-menu">
        <li><router-link to="/about">About</router-link></li>
      </ul>
  </div>
  <div id="second-view">
    <router-view />
  </div>
</div>
</template>

<style lang="sass">
  @import '@/assets/style/all.sass'
  html
    background: $bg
    color: $fg
    letter-spacing: 0.025rem
    line-height: 1.5
    #app
      width: 75%
      margin: 1rem auto
      padding: 1rem
      #menu-view
        width: 25%
        display: inline-block
        text-align: center
        #name
          width: 10rem
          margin: 0 auto
        #menu
          margin-top: 1rem
          .social
            padding: 1rem
          .social svg
            stroke: $fg
        #link-menu
          margin: 1.5rem 0 0 .5rem
          padding: 0
          li
            list-style-type: none
            a
              color: $fg
              text-decoration: none
              font-size: 1.75rem
              padding: 1rem 1rem .5rem 1rem
      #second-view
        display: inline-block
        width: 75%
</style>
