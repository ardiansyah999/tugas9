<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/todo">to do</router-link>
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
body {
  background-image: url("https://static.vecteezy.com/system/resources/previews/010/825/727/original/technology-background-modern-abstract-luxury-geometric-shape-premium-wallpaper-for-template-backdrop-brochure-poster-website-or-banner-free-vector.jpg"); /* ganti namafile.jpg dengan nama file gambar Anda */
  background-repeat: no-repeat;
  background-size: cover;
}

</style>
