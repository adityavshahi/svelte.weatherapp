<script>
    let currentTemprature = 32;
    let degreeSymbol = "\u00B0";
</script>


<style>
    @import url('https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,opsz,wght@0,6..12,200..1000;1,6..12,200..1000&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=PT+Sans:ital,wght@0,400;0,700;1,400;1,700&display=swap');
    div {
        font-family: "PT Sans", sans-serif;
        font-size: 3rem;
        display: flex;
        justify-content: center;
        flex-direction: column;
    }

    h1,p {
        margin: 0;
        padding: 0;
    }
    h1 {
        font-size: 7rem;
    }

    
</style>
    


<div>
    <h1>{currentTemprature}{degreeSymbol} C</h1>
    <p id="city-state">Pune, Maharashtra</p>
</div>