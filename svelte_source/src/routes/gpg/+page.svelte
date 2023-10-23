<script>
    import Navbar from "$lib/modules/navbar.svelte"

    let gpg_key = `-----BEGIN PGP PUBLIC KEY BLOCK-----

mDMEZRztFxYJKwYBBAHaRw8BAQdA44hGePqveyXnmWdNTGeEL5gKv6dChtdnUhq3
FU02wu20UkRpa3NoYW50IENoYW5kZWwgKFdlZCBPY3QgIDQgMTA6MTE6MzUgQU0g
SVNUIDIwMjMgLS0ga2V3QGFyY2gpIDxrZXdtaW5lQGdtYWlsLmNvbT6IkAQTFggA
OAIbAQIeAQIXgBYhBNzwfRvFV371tpVFs+b0bYG8K1pJBQJlHO2SBQsJCAcDBRUK
CQgLBRYCAwEAAAoJEOb0bYG8K1pJyHgA/0j2Z6dMc1cSyTdyxIWz8Lc97OzCX7m3
RkIHD2ejb5S4AQDt/MVaQaTuHyMAe02N6qjhSDAKgHEyi+K1wLovdbT9D7gzBGUc
7TgWCSsGAQQB2kcPAQEHQHA8fJLiUw0EokAKksflnBZG+48H9p6LsgglTgyBsD0i
iO8EGBYIACAWIQTc8H0bxVd+9baVRbPm9G2BvCtaSQUCZRztOAIbAgCBCRDm9G2B
vCtaSXYgBBkWCAAdFiEEYR/XQblz/cQAoPUNvltXUpUTZBUFAmUc7TgACgkQvltX
UpUTZBWjpAEAi8XP2wn1AHFwglzY4mAxJBuWk+lk5eK2kWk3ZUKYLLEA/RfoJ5x9
Jndvz8r/iLtv5E91uLyqI98dsVc5v0Yl49gJsqUA/0ONQgO5O2jMkUBeoYmh2lcy
bZZZ1lZsQhFi9HmnlFuBAPoClKGGqbLE//1lHpBs2AERkNQerLBx31llsU949jCV
DLg4BGUc7UkSCisGAQQBl1UBBQEBB0ADtHmjUOAVOIaooMkFHhjLj32tYlOl08BL
EkDNs0hqDgMBCAeIeAQYFggAIBYhBNzwfRvFV371tpVFs+b0bYG8K1pJBQJlHO1J
AhsMAAoJEOb0bYG8K1pJOM0BAMKInUu+ljtRu2L8L9iXlF8ISz4j1uwdW42syk3R
iSsPAQCF8aRZXYm3IuNXxtdCw4WGHgVzU97r8eMokzDkkrJCDg==
=UQZ7
-----END PGP PUBLIC KEY BLOCK-----`

    function copy_key() {
        navigator.clipboard.writeText(gpg_key);
        alert("copied")
    }

</script>

<Navbar/>
<div id="content">
    <div> ^_^</div>
    <pre>{gpg_key}</pre>
    <button on:click={copy_key}> copy to clipboard</button>
    <div>{status}</div>
</div>

<style lang="scss">
  @import "$lib/modules/theme";

  #content {
    padding: 2vh;
  }

  pre {
    font-family: "IBM Plex Mono", monospace;
    font-weight: 400;
    line-height: 2vh;
    font-size: 1.2vh;
    background-color: $bg_color;
    padding: 1.5vh;
  }

  button {
    font-family: "IBM Plex Mono",monospace;
    color: $fg_color;
    border: 2px solid $sakura;
    border-radius: 10px;
    padding: 1vh;
    background-color: $bg_color;
  }
</style>