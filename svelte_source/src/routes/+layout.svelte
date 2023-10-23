<svelte:head>
    <link rel="icon" href="{Favicon}" />
</svelte:head>

<script lang='ts'>
    import Favicon from "$lib/static/favicon.ico"
    import '../global.scss';
    import Footer from "$lib/modules/footer.svelte"
    import Pattern from "$lib/modules/bg-pattern.svelte"
</script>

<Pattern/>
<slot />
<Footer />

<style>


</style>