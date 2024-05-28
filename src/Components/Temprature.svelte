<script>
    let currentTemprature = 32;
    let degreeSymbol = "\u00B0";
</script>


<style>
    @import url('https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,opsz,wght@0,6..12,200..1000;1,6..12,200..1000&display=swap');
    div {
        font-family: "Nunito Sans", sans-serif;
        font-size: 1.8rem;
        position: absolute;
        left: 27.5%;
        top: 23%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
    }

    h1,p {
        margin: 0;
        padding: 0;
    }
</style>
    


<div>
    <h1>{currentTemprature}{degreeSymbol} C</h1>
    <p id="city-state">Pune, Maharashtra</p>
</div>