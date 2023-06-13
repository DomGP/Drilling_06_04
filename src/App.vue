<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col">
        <Gallery
        :gallery="gallery"
        @mostrarDesc="mostrar"/>
        
        </div>
        <div class="col">
          <Description
          :dataGallery="selectedImg"
          @cerrarBoton="clean"

          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Description from './components/Description.vue'
import Gallery from './components/Gallery.vue'

export default {
  name: 'App',
  components: {
    Gallery,
    Description
  },
  data(){
    return{
      gallery:[
        {url:"https://picsum.photos/id/237/600/400", author:'Bucky', desc:'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Temporibus, aspernatur!'},
        {url:"https://picsum.photos/id/238/600/400", author:'Bucky', desc:'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Temporibus, aspernatur!'},
        {url:"https://picsum.photos/id/239/600/400", author:'Bucky', desc:'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Temporibus, aspernatur!'}
      ],
      selectedImg:{}
    }
  },
  methods: {
    mostrar(index){
      this.selectedImg=this.gallery[index]
    },
    clean(){
      this.selectedImg={}
    }
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
