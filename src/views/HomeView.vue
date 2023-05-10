<template>
    <div class="home">
      <h1>Welcome To My Website </h1><br><hr><br>
      <p>Muhammad Ardiasnyah</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Home',
    components: { }
  }
  </script>

  <style>
body {
  font-family: 'Roboto', sans-serif;
  background-color: #F1F1F1;
  margin: 0;
  padding: 0;
}

.home {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h1 {
  font-size: 4rem;
  font-weight: 700;
  color: #333;
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin: 0;
  margin-bottom: 20px;
}

p {
  font-size: 1.5rem;
  font-weight: 500;
  color: #435342;
  text-align: center;
  margin: 0;
}

hr {
  width: 80%;
  height: 2px;
  background-color: #333;
  margin: 20px 0;
  border: none;
}

@media screen and (max-width: 768px) {
  h1 {
    font-size: 3rem;
  }

  p {
    font-size: 1.2rem;
  }

  hr {
    width: 60%;
  }
}

  </style>