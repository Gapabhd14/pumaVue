<template>  
    <model-obj id="model" src="../assets/3d/puma.obj"></model-obj>
    <!-- <div><p>חןכקךם</p></div> -->
</template>  

<script>  
    import { ModelObj } from 'vue-3d-model'
    export default {  
        components: { ModelObj }  
    }
</script> 

<style scoped>
#model{
    width: 20vw;
    height: 30vh;
}
</style>