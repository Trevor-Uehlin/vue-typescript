<template>

        <div class="weather-container p-6 h5 row">

            <div class="mt-4">
                <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                    Showing the weather for {{weather.city + ", " + weather.state}}
                </h2>            
            </div>
            

            <!-- <div class="col-3">
                <p class="h4">Currently</p>

                <div class="icon-container">
                    <img :src="weather.today.imageUrl" alt="weather icon" class="fa-2x">
                </div>
        
                <p>Mostly: {{weather.today.mostly}}.</p>
                <p>Description: {{weather.today.description}}</p>
                <p>Current Temperature: {{weather.today.currentTemp}}&#8457;</p>
                <p>Feels Like: {{weather.today.feelsLike}}&#8457;</p>
                <p>Max Temp: {{weather.today.maxTemp}}&#8457;</p>
                <p>Min Temp: {{weather.today.minTemp}}&#8457;</p>
                <p>Pressure: {{weather.today.pressure}}</p>
                <p>Humidity: {{weather.today.humidity}}&#37;</p>
                <p>Wind Speed: {{weather.today.windSpeed}} mph</p>
                <p>Visibility: {{weather.today.visibility}} miles</p>
            </div>

            <div class="text-center ml-5 forcast col">

                <p class="h4">7 Day Forcast</p>

                <div class="row ml-5 text-center">
        
                    <div v-for="daily in weather.forcast" :key="daily" class="m-4 col">
                        <p>{{daily.day}}</p>
                        <img :src="daily.imageUrl" alt="weather icon" class="icon">
                        <p>{{daily.maxTemp}}&#176; / {{daily.minTemp}}&#176;</p>
                    </div>
        
                </div>

            </div> -->

        </div>
</template>

<script lang="ts">

import { defineComponent } from "vue";

export default defineComponent ({
    data: function() {
        return {
            weather : [],
        }
    },
    props: {
        //weather: Array
    },
    mounted()  {
        this.getWeather();
        this.doTest();
    },
    methods:{
        getWeather(){
            fetch("http://fbf.com/api/test/weather")
                .then(resp => {
                    return resp.json();
                })
                .then(res2 => {
                    this.weather = res2;
                });
        },
        doTest(): void {
            console.log("Doing the test");
        }
    }

})
</script>

<style scoped>
.weather-container{
    background-color: blue;
    color:white;
}

.icon{
    height: 5rem;
}


@media screen and (max-width:750px) {

    .forcast{
        margin-top:40px;
    }
    .ml-5, .text-center{
        margin-left:unset !important;
    }
    
}
</style>