<script>
    import WhalburgerButton from "./WhalburgerButton.svelte";


    let modalEngaged = false

    function changeState() {
        modalEngaged = !modalEngaged;
    }

    $: modalEngagedDisplayValue = modalEngaged ? "block" : "none";

    $: modalStyle = `
      display: ${modalEngagedDisplayValue}; /* Hidden by default */
      position: fixed; /* Stay in place */
      z-index: 1; /* Sit on top */
      padding-top: 0px; /* Location of the box */
      left: 0;
      top: 0;
      width: 100%; /* Full width */
      height: 100%; /* Full height */
      overflow: auto; /* Enable scroll if needed */
    `
</script>



<WhalburgerButton {changeState}/>
<br>
stuffssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssssss

<!-- a transparent layer -->
<div style={modalStyle}>

  <div style="display: flex; height: 100%">

    <!-- modal content -->
    <div style="background-color: black; color: white;">
      <WhalburgerButton {changeState}/>
        <p style="padding-left: 20px; padding-right: 20px">Some text in the Modal..</p>
    </div>

    <!-- rest of space not used by modal -->
    <div style="background-color: rgb(0,0,0,0.2); flex: 1" on:click={changeState}>

    </div>

  </div>


</div>
