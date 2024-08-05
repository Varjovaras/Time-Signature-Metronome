<script>
    import { AppBar } from "@skeletonlabs/skeleton";
    import "../app.css";
</script>

<AppBar
    gridColumns="grid-cols-3"
    slotDefault="place-self-center"
    slotTrail="place-content-end"
>
    <svelte:fragment slot="lead">(icon)</svelte:fragment>
    (title)
    <svelte:fragment slot="trail">(actions)</svelte:fragment>
</AppBar>
<div
    class="flex flex-col items-center justify-center space-y-4 max-w-screen-xl min-h-screen mx-auto overflow-auto"
>
    <slot></slot>
</div>
