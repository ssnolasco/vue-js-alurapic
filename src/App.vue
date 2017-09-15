<template>
  <div>
    <h1>{{ titulo }}</h1>

    <ul>
      <li v-for="foto in fotos" :key="foto">
        <img :src="foto.url" :alt="foto.titulo" height="30%" width="30%">
      </li>
    </ul> 
  </div>
</template>

<script>
export default {
  data () {
    return {
      titulo: 'Alurapic',
      fotos: [
        {
          url: 'http://1.bp.blogspot.com/-tvZH8isFGzY/UKvsX4UTPlI/AAAAAAAACUs/xlqcvobMFAs/s1600/cachorros+famosos1.jpg',
          titulo: 'Cão 1'
        },
        {
          url: 'http://2.bp.blogspot.com/-qeB3PKXms5U/UKvnReGT0dI/AAAAAAAACUU/e-DOJpL6o3c/s1600/c%C3%A3es+famosos.jpg',
          titulo: 'Cão 2'
        },
        {
          url: 'http://1.bp.blogspot.com/-0JeRF9uDCV8/UKvo3-VzPGI/AAAAAAAACUc/82nTjmWlPNI/s1600/cachorros+mais+famosos.jpg',
          titulo: 'Cão 3'
        }
      ]
    }
  }
}
</script>

<style>

</style>
