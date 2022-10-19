<script>
    export let changeState;

    let buttonStyle = `
        font-size: 30px;
        height: 50px;
        width: 50px;
    `
</script>

<button on:click={changeState} style={buttonStyle}>☰</button>