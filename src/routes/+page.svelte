<script lang="ts">
    import Beep from "$lib/components/beep.svelte";
    import Slider from "$lib/components/slider.svelte";
</script>

<div
    class="flex flex-col items-center justify-center space-y-4 max-w-screen-xl min-h-screen mx-auto overflow-auto"
>
    <h1>Welcome to SvelteKit</h1>
    <p>
        Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation
    </p>
    <Beep />
    <Slider />
</div>
