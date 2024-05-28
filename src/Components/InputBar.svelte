<script>
    let city = '';

    function searchCity() {
        console.log(city);
        city = '';
    }
</script>

<style>
    #input-div {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-top: 1rem;
        margin-bottom: 1rem;
    }
    #input-bar {
        height: 5vh;
        width: 30vw;
        border-radius: 10px;
        font-size: 1.7rem;
        border: none;
        margin-right: 20px;
        padding: 5px;
    }

    #input-bar:focus {
        outline: none;
    }

    #search-button {
        height: 5.3vh;
        padding: 1rem;
        font-size: 1rem;
        border-radius: 8px;
    }
</style>


<div id="input-div">
    <input id="input-bar" bind:value={city} type="text" placeholder="City">
    <button on:click={searchCity} id="search-button">Search</button>
</div>