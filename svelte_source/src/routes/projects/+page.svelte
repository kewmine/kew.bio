<script>
    import Navbar from "$lib/modules/navbar.svelte"
</script>

<Navbar/>

<ul>
    <li>
        <div class="title"> OPULO <span class="title-desc">color palette</span> <span class="active">[active]</span>
        </div>
        <div class="desc">
            a color palette made for the best readability and is somewhat an eye-candy.
        </div>
        <div class="link"> link: <a href="https://opulo.ink">opulo.ink</a></div>
    </li>


    <li>
        <div class="title"> PILINK <span class="title-desc">link shortener</span> <span class="active">[active]</span>
        </div>
        <div class="desc">
            A suckless link shortener with a hits counter built using rust, mongodb and svelte.
        </div>
        <div class="link"> link: <a href="https://opulo.ink">pil.ink</a></div>
    </li>

    <li>
        <div class="title"> HEXITY <span class="title-desc">gameserver dispenser</span> <span class="discontinued">[discontinued]</span>
        </div>
        <div class="desc">
            A csgo server dispenser for various modes for players to grind in peace.
        </div>
        <div class="link"> link: <a href="https://hexity.org">hexity.org [disowned]</a></div>
    </li>

</ul>
<style lang="scss">
  @import "$lib/modules/theme";

  ul {
    padding-top: 1vh;
  }

  li {
    font-weight: 400;
    font-size: 2vh;
    padding: 3vh 0 3vh 0;
    margin: 2vh;
    border: 1px solid $sakura;
    border-radius: 10px;
    transition: 0.2s ease-in-out;
  }

  li:hover {
    background-color: $bg_color;
  }

  .title {
    font-family: "Robot", sans-serif;
    padding-left: 2vh;
    color: $sakura;
  }

  .title-desc {
    font-family: "Mooli", sans-serif;
    padding: 0 0 0 1vh;
    color: $washed;
  }

  .desc {
    font-family: "Mooli", sans-serif;
    color: $color_02;
    font-size: 1.8vh;
    padding: 1vh 2vh 0 2vh;
  }

  .link {
    padding-top: 1.5vh;
    font-size: 1.8vh;
    font-family: "IBM Plex Mono", monospace;
  }

  .active {
    font-size: 1.5vh;
    color: $toxic;
  }

  .discontinued {
    font-size: 1.5vh;
    color: $color_13;
  }
</style>
