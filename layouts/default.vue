<template>
  <div>
    <nav class = "navbar">
      <div class="navbar-brand">
        <figure class="image is-64x64">
          <img src="~static/dogpaw.png" alt="">
        </figure>
      </div>
      <div class="navbar-menu is-active">
        <div class="navbar-end">
          <nuxt-link to="/about" class="navber-item">소개</nuxt-link>
          <nuxt-link to="/stat" class="navbar-item">통계</nuxt-link>
        </div>
      </div>
    </nav>
    <nuxt/>
  <footer class="footer has-text-centered">
    <div>
        <figure class="image is-32x32">
         <img src="~assets/dog.png" alt="">
       </figure>2018.MOKWON</div>
  </footer>
  </div>
  </template>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
