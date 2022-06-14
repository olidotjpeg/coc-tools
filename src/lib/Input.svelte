<script lang="ts">
    let currentSanity = 0;
    let maxSanity = 0;

    let calculatedSanity = 0;

    function calculateSanity() {
        calculatedSanity = maxSanity - currentSanity;
    }
</script>

<div class="sanity">
    <h1>Are you insane?</h1>
    <div class="inputContainer">
        <input class="input" type="text" on:change={(e) => currentSanity = e.target.value} placeholder="Current Sanity">
        <div class="input-line"></div>
        <input class="input" type="text" on:change={(e) => maxSanity = e.target.value} placeholder="Max Sanity">
    </div>

    Damage Taken <div>{calculatedSanity}</div>

    <button on:click={calculateSanity}>Calculate Sanity</button>
</div>

<style>
    .sanity {
        display: flex;
        height: 100%;
        flex-direction: column;
        align-items: stretch;
    }

    h1 {
        text-align: center;
    }

    .inputContainer {
        position: relative;
        display: flex;
    }

    .input {
        border: 1px solid #000;
        width: 100%;
        text-align: center;
        height: 100px;
    }

    .input-line {
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translateY(-50%);
        width: 2px;
        height: 80%;
        background: tomato;
    }
    .input:first-of-type {
        border-right: none;
    }

    .input:last-of-type {
        border-left: none;
    }

</style>
