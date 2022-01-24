<template>
  <div v-if="result" class="about">

    <h1 Class=WEATHER>WEATHER</h1>
  
    <p Class=Weather>Weather: {{ result.weather[0].description  }}</p>
<p Class=timezone> timezone: {{ result.name }}</p>
   <p Class=Clouds>Clouds: {{ result.clouds.all  }}</p>
    <p Class=main>main: {{ result.main  }}</p>
    <p Class=coord>coord: {{ result.coord }} </p>
    <p Class=visibility>visibility: {{ result.wind }}</p>
    
   
  </div>
</template>
<script>
import axios from "axios";
export default {
  data: () => ({

    result: null,
    
  }),
  created() {
  
      
    axios.get("https://api.openweathermap.org/data/2.5/weather?q=playa%20del%20carmen&APPID=e8b2336696e9c9fc1d4bec1bbe67a43c").then((result) => {
      console.log(result.data);
      this.result = result.data;
    });
      
  }
      
  }

</script>
<style>


* {
  margin: 50px;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: 'montserrat', sans-serif;
  height:600px;
  background-image: url("https://i.pinimg.com/736x/c0/b7/1f/c0b71f926fa36368906e4652d0286b6f.jpg");
  
}

.WEATHER{
  margin: 0;
  padding: 1px;
  box-sizing: border-box;
  box-shadow: 0px 0px 16px rgba(32, 28, 28, 0.25);
  background-color: rgba(175, 128, 162, 0.75);
  border-radius: 16px 0px 16px 0px;
}
.Clouds {
  font-family: 'montserrat', sans-serif;
color:midnightblue;;
font-weight: bold;
border-radius: 16px;
  margin: 30px 0px;

}

.main {
color:midnightblue;
font-weight: bold;
border-radius: 16px;
  margin: 30px 0px;

}
.coord {
color:midnightblue;
font-weight: bold;
border-radius: 16px;
  margin: 30px 0px;

}

.visibility {
color:midnightblue;
font-weight: bold;
border-radius: 16px;
  margin: 30px 0px;

}
.timezone {
color:midnightblue;
font-weight: bold;
border-radius: 16px;
  margin: 30px 0px;

}
.Weather {
color:midnightblue;
font-weight: bold;
border-radius: 16px;
  margin: 30px 0px;

}

</style>>


  
