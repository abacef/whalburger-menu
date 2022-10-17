<script lang="ts">
  let open = false

  function changeWhalburger() {
    open = !open
  }
</script>


<table>

  <tr>
    <td>
      <button on:click={changeWhalburger}>
        ☰
      </button>
    </td>
  </tr>

  
  <!-- {#if open}
    <tr>
      one option
    </tr>
    <tr>
      2 opt
    </tr>
  {/if} -->

</table>
