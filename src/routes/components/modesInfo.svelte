<script lang="ts">
    import { onMount } from "svelte";
    import { writable } from "svelte/store";

    const selectedMode = writable("SMP");

    onMount(() => {
        const videoElement = document.getElementById("video") as HTMLVideoElement;

        selectedMode.subscribe((mode) => {
            if (!videoElement) return;

            if (mode === "SMP") {
                videoElement.src = "modesInfoVideos/video.webm";
            }
            if (mode === "inny tryb") {
                videoElement.src = "modesInfoVideos/video2.webm";
            }
            if (mode === "itd") {
                videoElement.src = "modesInfoVideos/video3.webm";
            }
            if (mode === "itp") {
                videoElement.src = "modesInfoVideos/video4.webm";
            }

            videoElement.load(); // Załaduj nowy film po zmianie src
        });
    });
</script>
<div id="modesInfo-container">
    <div id="modesInfo-left">
        <button onclick={() => selectedMode.set("SMP")} class:active={$selectedMode === "SMP"}>SMP</button>
        <button onclick={() => selectedMode.set("inny tryb")} class:active={$selectedMode === "inny tryb"}>inny tryb</button>
        <button onclick={() => selectedMode.set("itd")} class:active={$selectedMode === "itd"}>itd</button>
        <button onclick={() => selectedMode.set("itp")} class:active={$selectedMode === "itp"}>itp</button>        
    </div>
    <div id="modesInfo-right">
        <video id="video" autoplay muted disablepictureinpicture>
            <track kind="captions" src="video-captions_en.vtt" srclang="en" label="English">
        </video>
    </div>
</div>

<style>
    #modesInfo-container{
        height: 800px;
        display: flex;
        background-color:bisque;
    }

    #modesInfo-left{
        display: flex;
        flex-direction: column;
        position: absolute;
        width: 250px;
        height: 800px;
    }

    #modesInfo-right{
        width: 100%;
        background-image: url("https://static.wikia.nocookie.net/minecraft_gamepedia/images/c/c8/Block_of_Coal_%28texture%29_JE3_BE2.png");
    }

    video{
        width: 100%;
        height: 100%;
    }

    #modesInfo-left button {
        width: calc(100% - 30px);
        height: 50px;
        background-color: rgba(0, 0, 0, 0.329);
        color: white;
        font-size: 20px;
        border: 1px solid white;
        cursor: pointer;
        transition: width 0.2s ease-in-out;
    }

    .active {
        width: 100% !important; 
    }

    #modesInfo-left button:hover:not(.active) {
        width: calc(100% - 25px);
    }
</style>
