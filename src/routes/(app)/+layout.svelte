<script lang='ts'>
    import Navbar from '$lib/components/Navbar.svelte';
    import '../../app.css';
</script>

<style>
    :global(.custom-icon) {
        width: 28px;
        height: 28px;
    }
</style>
    <Navbar/>
    <slot />


