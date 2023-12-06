<template>
  <div>
  <!-- Step 3: use the component -->
  <MyHeader headingName="TOP FIVE TALLEST BUILDINGS IN WORLD" creatorName ="Website created by JAWAHAR RAVULAPALLI" />
  <BuildingBox :buildings="buildings" />
 <p> Data reference-'https://www.skyscrapercenter.com/buildings' </p>
</div>
</template>

<script>
// STep 1 : you import the component
import MyHeader from './components/MyHeader.vue'
import BuildingBox from './components/BuildingBox.vue'


export default{
  name: 'App',
  // Step 2: register the component
  components:{
    MyHeader,
    BuildingBox 
  },
  data(){
    return {
      buildings: []
    }
  },
  mounted(){
    fetch('https://final-node-server-c0z5.onrender.com/api')
    .then(res=>res.json())
    .then(data=>{this.buildings = data.buildings;})
    .catch(err=>console.log(err.message))

  }
}
</script>

<style >

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
  background-color: beige;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}
p{
text-align: right;
padding-right: 5px;
}


</style>