<script lang="ts">
    import Navbar from "$lib/modules/navbar.svelte"
    import Blinker from "$lib/modules/blinker.svelte"
    import Data from '$lib/data.json';
</script>

<div class="section">
    <div id="display">
        <div id="title">
            <div id="name">{Data["author"]}</div>
            <Blinker/>
        </div>
        <div id="desc">{Data["description"]}</div>
    </div>
</div>
<Navbar/>

<style lang="scss">
  @import "$lib/modules/theme";

  #title {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }


  #display {
    padding: 3vh 0 5vh 0;
    color: $fg_color;
  }

  #name {
    letter-spacing: 5px;
    justify-content: center;
    align-items: center;
    align-self: center;
    color: $fg_color;
    font-size: 5.5vh;
  }

  #desc {
    font-family: "IBM Plex Mono", monospace;
    font-weight: 400;
    color: $clouds;
  }
</style>
