<template>
    <div>
        <div class="row">
            <div class="col">
                <img :src="dataGallery.url" alt="">
                <div>
                    Autor:{{dataGallery.author}}
                </div>
            </div>
            <button @click="cerrarBoton">Cerrar</button>
            <div class="col">
                {{dataGallery.desc}}
            </div>
        </div> 
    </div>
</template>

<script>
export default {
    name: 'component-name',
    props: {
        dataGallery:{
            type: Object,
            required:true,
        }
    },
    data: function(){
        return {}
    },
    // computed: {},
    methods: {
        cerrarBoton(){
            this.$emit('cerrarBoton')
        }
    }
    // watch: {},
    // components: {},
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped>
    
</style>