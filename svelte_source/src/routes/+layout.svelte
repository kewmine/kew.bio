<script lang='ts'>
    import Favicon from "$lib/static/favicon.ico"
    import '../global.scss';
    import Footer from "$lib/modules/footer.svelte"
    import Pattern from "$lib/modules/bg-pattern.svelte"
    import data from '$lib/data.json';
</script>

<svelte:head>
    <link rel="icon" href="{Favicon}"/>
    <title>{data['author']}</title>
    <meta name="description" content="{data['site_desc']}"/>
    <meta property="og:title" content="{data['site_desc']}"/>
    <meta property="og:url" content="https://{data['domain']}"/>
    <meta property="og:image" content="{data['site_cover']}"/>
</svelte:head>
<Pattern/>
<slot/>
<Footer/>

<style>


</style>