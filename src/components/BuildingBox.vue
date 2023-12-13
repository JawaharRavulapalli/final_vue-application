<template>
   <div>
    <!-- Step 3: use the component -->
    <div v-for="tower of buildings" :key="tower.id">
    
    <TowerBox :tower=tower />
</div>   
</div>

</template>

<script>
// STep 1 : you import the component
import TowerBox from './TowerBox.vue' 
export default{
    name: 'BuildingBox',
    props:{
        buildings: Array
    },
    // Step 2: register the component
    components:{
        TowerBox
    }
}

</script>

<style scoped>
div{
    text-align: center;
    
}

</style>
