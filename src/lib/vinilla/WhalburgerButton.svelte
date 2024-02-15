<script>
    export let changeState;

    export let modalEngaged;

    $: textColor = modalEngaged ? "white" : "black"

    $: buttonStyle = `
        font-size: 30px;
        height: 50px;
        width: 50px;
        background-color: Transparent;
        color: ${textColor}
    `

</script>

<button on:click={changeState} style={buttonStyle}>☰</button>