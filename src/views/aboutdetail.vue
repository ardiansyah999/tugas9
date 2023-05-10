<template>
    <h1>Tentang Diri Saya</h1>
    <p>Pecinta Program {{ id }}</p>
</template>

<script>
export default {
    props: ['id'],
    // data() {
    //     return {
    //         id: this.$route.params.id
    //     }
    // }
}
</script>
<style>
/* CSS untuk container */
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f5f5f5;
}

/* CSS untuk judul */
h1 {
  font-size: 4rem;
  text-align: center;
  margin-bottom: 2rem;
  color: #333;
}

/* CSS untuk deskripsi */
p {
  font-size: 2rem;
  text-align: center;
  color: #666;
}

/* CSS untuk animasi */
.pulse {
  animation-name: pulse;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in-out;
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}

/* CSS untuk media query */
@media (max-width: 768px) {
  h1 {
    font-size: 3rem;
  }
  p {
    font-size: 1.5rem;
  }
}
</style>