<nav>
    <a class="item" href="/projects">PROJECTS</a>
    <a class="item" href="/whoami">WHOAMI</a>
    <a class="item" href="/connect">CONNECT</a>
    <a class="item" href="/">HOME</a>
</nav>

<style lang="scss">
  @import "theme";

  nav {
    display: flex;
    max-width: fit-content;
    justify-self: center;
    align-items: center;
    margin: 1vh 0 1vh 0;
    border: 2px solid $sakura;
  }

  a {
    color: $fg_color;
    padding: 1vh 2vh 1vh 2vh;
    margin: 0;

    font-family: "IBM Plex Mono", monospace;
    font-weight: 400;
    font-size: 1.8vh;
  }

  a:hover, a:active {
    color: $bg_color;
    background-color: $clouds;
  }

</style>