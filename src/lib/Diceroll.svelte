<script lang="ts">
    let diceRoll = 0;
    let diceState = '';

    function handleDiceRoll() {
        const min = 0;
        const max = 100;

        diceState = '';

        diceRoll = Math.floor(Math.random() * (max - min + 1) + min)

        if (diceRoll === 0) {
            diceState = 'FUMBLE';
        } else if (diceRoll >= 96) {
            diceState = 'FUMBLE';
        } else if (diceRoll === 1) {
            diceState = 'CRITICAL';
        }
    }
</script>

<div class="container">
    <p class={`state ${diceState}`}>{diceState}</p>
    <button class="diceBtn" on:click={handleDiceRoll}>Dice Roll | {diceRoll}</button>
</div>

<style>
    .container {
        height: 60px;
    }

    .diceBtn {
        background: orange;
        color: #fff;
        border: 0;
        padding: 12px;
        width: 100%;
    }

    .state {
        margin: 0;
        height: 18px;
    }

    .FUMBLE {
        color: red;
    }

    .CRITICAL {
        color: green;
    }
</style>