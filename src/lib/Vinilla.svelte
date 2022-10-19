<script>

    let showCss = "block"
    function changeState() {
        if (showCss == "none") {
            showCss = "block"
        } else {
            showCss = "none"
        }
    }

    $: modalStyle = `
      display: ${showCss}; /* Hidden by default */
      position: fixed; /* Stay in place */
      z-index: 1; /* Sit on top */
      padding-top: 100px; /* Location of the box */
      left: 0;
      top: 0;
      width: 100%; /* Full width */
      height: 100%; /* Full height */
      overflow: auto; /* Enable scroll if needed */
      background-color: rgb(0,0,0); /* Fallback color */
      background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
    `

    $: modalContent = `
      background-color: #fefefe;
      margin: auto;
      padding: 20px;
      border: 1px solid #888;
      width: 80%;
    `
</script>


<!-- Trigger/Open The Modal -->
<button on:click={changeState} style="font-size : 30px; height:50px; width:50px;">☰</button>

<!-- The Modal -->
<div id="myModal" style={modalStyle}>

  <!-- Modal content -->
  <div style={modalContent}>
    <button on:click={changeState}>closeModel</button>
    <p>Some text in the Modal..</p>
  </div>

</div>
