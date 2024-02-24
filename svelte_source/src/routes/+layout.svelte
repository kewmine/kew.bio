<script lang="ts">
  import Favicon from "$lib/static/favicon.ico";
  import "../global.scss";
  import Footer from "$lib/modules/footer.svelte";
  import Pattern from "$lib/modules/bg-pattern.svelte";
  import data from "$lib/data.json";

  import { animate } from "motion";
  import { onMount } from "svelte";
  onMount(() => {
    animate(
      ".content",
      { opacity: 1, transform: "none" },
      { delay: 0, duration: 0.9, easing: [0.17, 0.55, 0.55, 1] }
    );
  });
</script>

<svelte:head>
  <link rel="icon" href={Favicon} />
  <title>{data["author"]}</title>
  <meta name="description" content={data["site_desc"]} />
  <meta property="og:title" content={data["site_desc"]} />
  <meta property="og:url" content="https://{data['domain']}" />
  <meta property="og:image" content={data["site_cover"]} />
</svelte:head>

<div class="content">
  <Pattern />
  <slot />
  <Footer />
</div>

<style>
    .content {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        opacity: 0;
    }
</style>
