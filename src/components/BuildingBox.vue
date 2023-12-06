<template>
   <div>
    
    <div v-for="tower of buildings" :key="tower.id">
    
    <TowerBox :tower=tower />
</div>   
</div>

</template>

<script>

import TowerBox from './TowerBox.vue' 
export default{
    name: 'BuildingBox',
    props:{
        buildings: Array
    },
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
