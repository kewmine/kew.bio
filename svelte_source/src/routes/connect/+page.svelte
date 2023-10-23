<script>
    import Navbar from "$lib/modules/navbar.svelte"
    import data from '$lib/data.json';
</script>

<Navbar/>

<div class="info">
    <div>/ emails from shady domains are filtered /</div>
</div>

<div id="table">
    <table>
        <tr>
            <th class="category"> telegram:</th>
            <th><a href="https://t.me/{data['telegram']}">{data['telegram']}</a></th>
        </tr>

        <tr>
            <th class="category"> email:</th>
            <th><a href="mailto:{data['email']}">{data['email']}</a></th>
        </tr>

        <tr>
            <th class="category"> pgp:</th>
            <th><a href="/gpg"> gpg key</a></th>
        </tr>
    </table>
</div>

<style lang="scss">
  @import "$lib/modules/theme";

  .info {
    max-width: 60vh;
    font-family: "IBM Plex Mono", monospace;
    line-height: 2.5vh;
    letter-spacing: 0.04vh;
    font-weight: 400;
    font-size: 1.7vh;
    color: $clouds;
    padding: 10vh 0 3vh 0;
  }

    #table {
        font-size: 2.2vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    table {
        justify-content: center;
        align-items: center;
        text-align: left;
        border: 1px solid $sakura;
        padding: 2vh 2vh 2vh 2vh;

    }

    th {
        font-weight: 400;
    }

    .category {
        color: $washed;
        padding-right: 3vh;
        font-family: "IBM Plex Mono", monospace;
    }

</style>

