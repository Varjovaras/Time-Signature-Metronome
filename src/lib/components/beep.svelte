<script lang="ts">
    import { onMount } from "svelte";

    export const autoplay = false;
    const src = "/beep.mp3";
    let audio: HTMLAudioElement | null = null;

    function play() {
        audio?.play();
    }

    function pause() {
        audio?.pause();
    }

    onMount(() => {
        audio = new Audio(src);
        if (autoplay) {
            audio.play();
        }
    });
</script>

<button on:click={play}>Play</button>
<button on:click={pause}>Pause</button>
