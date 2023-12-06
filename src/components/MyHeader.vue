<template>
    <div>
        <h2> {{headingName}}</h2>
        <h2>{{creatorName}} </h2>
        
    </div>
</template>

<script>

    export default{
        name: 'MyHeader',
        props:{
            creatorName: String,
            headingName: String
        }

    }
 
</script>

<style scoped>
    div{
        text-align: center;
        color: brown;
    }

</style>
