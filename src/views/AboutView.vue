<template>
    <div v-for="abouts in about" :key="abouts.id" class="about">
      <router-link :to="{name: 'AboutDetails', params: { id: abouts.id }}">
        <h2>{{ abouts.tittle }}</h2>
      </router-link>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        about: [
          { tittle: 'Mahasiswa Teknik Informatika', id: 1, details: 'lorem' },
          { tittle: 'Contact Me', id: 2, details: 'lorem' },
          
        ]
      }
    }
  }
  </script>
  
  <style>
 /* Styling for about section */
.about {
  background-color: #4f7a85;
  border-radius: 10px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  padding: 20px;
  margin: 20px 0;
  text-align: center;
  transition: all 0.3s ease-in-out;
}

.about:hover {
  transform: translateY(-5px);
  box-shadow: 0px 5px 20px rgba(0, 0, 0, 0.2);
}

.about h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

.about a {
  text-decoration: none;
  color: #42b983;
}

  </style>