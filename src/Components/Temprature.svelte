<script>
    let currentTemprature = 32;
    let feelsLikeTemprature = 33;
    let degreeSymbol = "\u00B0";
    export let weatherData;
</script>


<style>
    @import url('https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,opsz,wght@0,6..12,200..1000;1,6..12,200..1000&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=PT+Sans:ital,wght@0,400;0,700;1,400;1,700&display=swap');
    div {
        font-family: "PT Sans", sans-serif;
        display: flex;
        justify-content: center;
        flex-direction: column;
    }

    h1,p {
        margin: 0;
        padding: 0;
        font-size: 3rem;
    }
    h1 {
        font-size: 7rem;
    }

    i {
        font-size: 2rem;
    }

    #weather-type {
        font-size: 1.5rem;
    }

    
</style>
    


<div>
    <h1>{weatherData.temprature}{degreeSymbol} C</h1>
    <p id="weather-type">{weatherData.weatherType}</p>
    <p id="city-state">{weatherData.cityName}, {weatherData.region}</p>
    <i>Feels Like : {weatherData.feelslike}{degreeSymbol} C</i>
</div>