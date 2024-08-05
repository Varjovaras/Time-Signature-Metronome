<script lang="ts">
    import { onMount } from "svelte";
    const BEEP_LOCATION = "/beep.mp3";
    let autoplay = true;
    let audio: HTMLAudioElement;
    let intervalId: NodeJS.Timeout | null = null;
    let intervalAsMilliseconds = 600;

    function play() {
        audio.play();
        if (!intervalId) {
            intervalId = setInterval(() => {
                if (autoplay) {
                    audio.play();
                } else {
                    if (intervalId) {
                        clearInterval(intervalId);
                        intervalId = null;
                    }
                }
            }, intervalAsMilliseconds);
        }
    }

    function pause() {
        autoplay = false;
        if (intervalId) {
            clearInterval(intervalId);
            intervalId = null;
        }
        audio.pause();
    }

    onMount(() => {
        audio = new Audio(BEEP_LOCATION);
    });
</script>

<button on:click={play}>Play</button>
<button on:click={pause}>Pause</button>
