<script>
  import Navbar from "$lib/modules/navbar.svelte";
  import data from "$lib/data.json";
  import Git_logo from "$lib/static/git.png";
  import Ctftime_logo from "$lib/static/ctftime.png";
  import Twitter_logo from "$lib/static/twitter.png";
  import Hackthebox_logo from "$lib/static/hackthebox.png";
  import Leetcode_logo from "$lib/static/leetcode.png";
  import Linkedin_logo from "$lib/static/linkedin.png";
  import Data from "$lib/data.json";
</script>

<Navbar />

<div class="info">
  I am an experimentalist with a security background who likes coding resilient
  and performant apps in Rust. Check out my blog for recent updates.
</div>
<div id="table">
  <table>
    <tr>
      <th class="category"> forte:</th>
      <th>{data["forte"]}</th>
    </tr>

    <tr>
      <th class="category"> codes in:</th>
      <th>{data["codes_in"]}</th>
    </tr>

    <tr>
      <th class="category"> worked with:</th>
      <th> {data["my_ex"]}</th>
    </tr>

    <tr>
      <th class="category"> what else?</th>
      <th>{data["what_else"]}</th>
    </tr>
  </table>
</div>
<div class="socials">
  <div>
    <a href="https://github.com/{Data['github']}">
      <img class="logo" src={Git_logo} alt="github" />
    </a>
  </div>

  <div>
    <a href="https://ctftime.org/user/{Data['ctftime']}">
      <img class="logo" src={Ctftime_logo} alt="ctftime" />
    </a>
  </div>

  <div>
    <a href="https://app.hackthebox.com/profile/{Data['hackthebox']}">
      <img class="logo" src={Hackthebox_logo} alt="hackthebox" />
    </a>
  </div>

  <div>
    <a href="https://twitter.com/{Data['twitter']}">
      <img class="logo" src={Twitter_logo} alt="twitter" />
    </a>
  </div>

  <div>
    <a href="https://leetcode.com/{Data['leetcode']}">
      <img class="logo" src={Leetcode_logo} alt="twitter" />
    </a>
  </div>
  <div>
    <a href="https://www.linkedin.com/in/{Data['leetcode']}">
      <img class="logo" src={Linkedin_logo} alt="twitter" />
    </a>
  </div>
</div>

<style lang="scss">
  @import "$lib/modules/theme";

  .socials {
    display: inline-flex;
    padding: 1vh;
    margin: 1vh 0 4vh 0;
  }

  .logo {
    border: 0.5vh solid $color_03;
    border-radius: 10px;
    margin: 0.4vh;
    height: 4vh;

    -moz-transition: all 0.2s ease-in;
    -o-transition: all 0.2s ease-in;
    -webkit-transition: all 0.2s ease-in;
    transition: all 0.2s ease-in;
  }

  .logo:hover,
  .logo:active {
    border: 0.5vh solid $color_04;
    margin: 0.4vh;
    height: 4vh;
  }

  .info {
    max-width: 60vh;
    font-family: "IBM Plex Mono", monospace;
    line-height: 2.5vh;
    letter-spacing: 0.04vh;
    font-weight: 400;
    font-size: 1.7vh;
    color: $clouds;
    padding: 10vh 0 5vh 0;
  }

  #table {
    font-size: 2.2vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  table {
    margin: 0.5em;
    text-align: left;
    border: 1px solid $sakura;
    padding: 2vh 2vh 2vh 2vh;
  }

  th {
    font-weight: 400;
    max-width: 30vh;
    text-align: left;
  }

  .category {
    max-width: 20vh;
    color: $washed;
    padding: 1vh 0.5vh 0.2vh 1vh;
    font-family: "IBM Plex Mono", monospace;
    font-size: 0.9em;

    text-align: left;
  }
</style>
