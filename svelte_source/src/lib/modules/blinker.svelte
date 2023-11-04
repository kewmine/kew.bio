<div id="link">.</div>

<style lang="scss">
  @import "theme";

  #link {
    font-weight: 400;
    font-size: 10vh;
    line-height: 3.5vh;

    animation: blink 0.5s linear infinite;
    user-select: none;
    pointer-events: none;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    -webkit-user-drag: none;
  }

  @keyframes blink {
    0%,
    20%,
    50%,
    80% {
      color: $bg_color;
      text-shadow: none;
    }
    30%,
    70%,
    95% {
      color: $blinker_color;
      text-shadow: 0 0 10px $blinker_color, 0 0 20px $blinker_color, 0 0 40px $blinker_color,
      0 0 80px #fff;
    }
  }
</style>