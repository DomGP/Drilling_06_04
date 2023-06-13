<template>
    <div class="img-style">
        <div v-for="(imagen,index) in gallery" :key="index">
            <img :src="imagen.url" alt="" @click="mostrarDesc(index)">
        </div>
    </div>
</template>

<script>
export default {
    name: 'component-name',
    props: {
        gallery:{
            type:Array,
            required:true,
        }
    },
    data: function(){
        return {}
    },
    // computed: {},
    methods: {
        mostrarDesc(index){
            this.$emit('mostrarDesc',index)
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
    .img-style{
        max-height: 900px;
        overflow: auto;
    }
</style>