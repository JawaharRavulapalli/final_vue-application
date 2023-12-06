<template>
    <div>
    <h2>Rank- {{ tower.rank }}</h2>
    <h2>Name- {{ tower.name }}</h2>
    <h2>City- {{ tower.city }}</h2>
    <h2>Height in meters- {{ tower.height}}</h2>
    <h4>Year of completion- {{ tower.year_completed}}</h4>
    <h4>Status of Completion- {{ tower.completion_status}}</h4>
    <h4>Function of tower- {{ tower.function}}</h4>

    </div>
</template>

<script>

    export default{
        name: 'TowerBox',
        props:{
            tower: Array
        }

    }
 
</script>

<style scoped>


.green{
    background-color: green;
}

h4{
    margin: 2px;
}

div{
    background-color: #f3c3b1;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    border: 7px solid skyblue;
    

}


h2{

    font-size: 1em;

}

</style>
