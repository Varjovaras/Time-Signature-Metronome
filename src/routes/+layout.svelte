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

<slot></slot>
