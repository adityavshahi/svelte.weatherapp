<script>
    import InputBar from "./InputBar.svelte";
    import token from "../../token";
    import Temprature from "./Temprature.svelte";
    import {onMount} from 'svelte';

    let city = "";
    let data = null;
    let visible = false;
    let weatherData = {};

    async function fetchWeatherData(city) {
        console.log(`Fetching weather for city : ${city}`);
        let url = `http://api.weatherapi.com/v1/current.json?key=${token}&q=${city}/&aqi=yes`;
        const response = await fetch(url);
        const data = await response.json();
        weatherData = {
            cityName: data.location.name,
            region:data.location.region,
            weatherType: data.current.condition.text,
            temprature: data.current.temp_c,
            feelslike: data.current.feelslike_c
        }
        visible = true;
    }

    function handleCitySelected(event) {
        city = event.detail.city;
        fetchWeatherData(city).then(() => {
            visible = true
        });
    }
</script>


<style>
    #weatherinfo {
        height: 70vh;
        width: 50vw;
        border-radius: 20px;
    }
    .hidden {
        display: none;
    }
    .visible {
        display: block;
    }
</style>

<InputBar on:citySubmitted={handleCitySelected} />

<div id="weatherinfo" class:visible={visible} class:hidden={!visible}>
    <Temprature {weatherData} />
</div>