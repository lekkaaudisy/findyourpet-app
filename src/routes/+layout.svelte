<script lang='ts'>
    import Sidebar from '$lib/components/Sidebar.svelte';
    import '../app.css';
</script>

<style>
    :global(.custom-icon) {
        width: 28px;
        height: 28px;
    }
</style>
    <Sidebar/>
    <slot />


