<template>
<div>
  <!-- Image and text -->
  <b-navbar variant="faded" type="light">
    <b-navbar-brand href="#">
      <b-img src="https://i.pinimg.com/originals/df/24/54/df2454d59ad43d71656fbe3342367b9a.png" rounded class="d-inline-block align-top img" alt="Kitten"/>
      <span class="title-app"> Clima APP </span>
    </b-navbar-brand>
  </b-navbar>
</div>
</template>

<script>
export default {
data(){
    return{

    }
}
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Gemunu+Libre&display=swap');
.img{
    width: 50px;
    height: 50px;
    margin-top: 15px;
}
.title-app{
    font-family: 'Gemunu Libre', sans-serif;
    font-size: 3em;
}
</style>