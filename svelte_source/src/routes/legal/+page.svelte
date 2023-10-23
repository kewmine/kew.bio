<script>
    import Navbar from "$lib/modules/navbar.svelte"
</script>

<Navbar/>
<div class="legalbox">
    <ul>
        <div class="legal-heading">Illicit content &amp; ownership:</div>
        <li>
            I do not have control over what users may upload to my server.<br/>
            However, you can <a class="toxic" href="/connect/">report illicit activities to me via
            connect</a> page<br/>
            and it will be taken down asap.
        </li>
        <li>
            <span class="toxic">I reserve the right to purge any content</span><br/>
            uploaded by me or the user if I deem that unfit.
        </li>

        <div class="legal-heading">Third-party resources:</div>
        <li>
            I might add links to third-party resources in blog posts and
            archive<br/>
            which could later be changed into something malicious.<br/>
            <span class="toxic" >Be mindful of what you're doing.</span>
        </li>


        <div class="legal-heading">Have a query?</div>
        <li>
            My contact info is on the
            <a class="toxic" href="/connect/">connect </a>page, feel free
            to message me.
        </li>

    </ul>
</div>

<style lang="scss">
    @import "$lib/modules/theme";

    .legalbox {
        font-weight: 400;
        text-align: left;
        padding: 4vh 0 4vh 0;
    }

    .toxic {
      color: $toxic;
    }

    .legal-heading {
        color: $sakura;
        padding: 5vh 0 1vh 0;
    }

    ul {
        list-style: square;
        max-width: 90vw;
    }

    li {
        font-family: "IBM Plex Mono", monospace;
        font-size: 1.5vh;
    }
</style>