<script>
    export let changeState;
    export let modalEngaged;
</script>

<style>
    .button {
        font-size:  30px;
        height:  50px;
        width:  50px;
        background-color: transparent;
    }

    .button--dark {
        color: black;
    }

    .button--light {
        color: white;
    }
</style>

<button class="button {modalEngaged ? 'button--light' : 'button--dark'}" on:click={changeState}>☰</button>