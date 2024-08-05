<script lang="ts">
    import { RangeSlider } from "@skeletonlabs/skeleton";

    let value = 15;
    let max = 25;
</script>

<div class="w-6/12">
    <!-- <div class="flex flex-col justify-center px-8 mb-8"> -->
    <RangeSlider name="range-slider" bind:value {max} step={1} ticked>
        <div class="flex justify-between items-center">
            <div class="font-bold">Label</div>
            <div class="text-xs">{value} / {max}</div>
        </div>
    </RangeSlider>
</div>
