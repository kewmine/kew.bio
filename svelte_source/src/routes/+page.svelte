<script lang="ts">
  import Navbar from "$lib/modules/navbar.svelte";
  import Blinker from "$lib/modules/blinker.svelte";
  import Data from "$lib/data.json";

  import { animate } from "motion";
  import { browser } from "$app/environment";

  if (browser) {
    animate(
      "section",
      { opacity: 1, transform: "none" },
      { delay: 0.5, duration: 0.9, easing: [0.17, 0.55, 0.55, 1] }
    );
  }
</script>

<section>
  <div class="section">
    <div id="display">
      <div id="title">
        <div id="name">{Data["author"]}</div>
        <Blinker />
      </div>
      <div id="desc">{Data["description"]}</div>
    </div>
  </div>
  <Navbar />
</section>

<style lang="scss">
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    opacity: 0;
  }

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
