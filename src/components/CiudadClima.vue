<template>
    <div>
         <b-img :src="getImageFromClima" fluid></b-img>
    </div>
</template>

<script>
export default {
data(){
    return{
        cityWeather: {},
        imageWeather: null,
        ciudad: 'caracas',
        appid: 'f7ca6a322124f9a89917c96f222940dc',
       
    }
},
created(){
    this.getClima();
},
methods:{
    //f7ca6a322124f9a89917c96f222940dc
    getClima(){
        window.axios = require('axios');
        axios.get('http://api.openweathermap.org/data/2.5/weather', {
            params:{
                q: this.ciudad,
                appid: this.appid,
                lang: 'sp'
            }
    })
    .then((response) => {
        this.cityWeather = response.data
    })
    .catch((error) => {
        console.log(error);
    })
    .finally((e) =>{
        // always executed
    }); 
    }
},
computed:{
  getImageFromClima(){
      var url = '';
      switch (this.cityWeather.weather[0].main) {
        case 'Clear':
            url = 'https://st4.depositphotos.com/22320054/i/600/depositphotos_255688108-stock-photo-fuffy-clouds-on-bright-blue.jpg';
            break;

        case 'Rain':
            url = 'https://mocah.org/uploads/posts/4598931-faze-rain-rain-city-glass-water-drops-window-bokeh-water-on-glass-lights.jpg';
            break;

        case 'Clouds':
            url = 'https://cdn.pixabay.com/photo/2020/01/25/22/42/clouds-4793523_960_720.jpg';
            break;

        default:
            break;
      }
      return url;
  }
}

}
</script>

<style scoped>
.img{
    width: 100%;
}
</style>