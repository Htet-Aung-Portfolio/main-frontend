<script>
    import Welcome from "./Pages/welcome.svelte";

    export let name;
</script>

<svelte:head>
    <title>
        {name} | Welcome
    </title>
</svelte:head>

<main class="content_displayer">
    <audio autoplay loop>
        <source src="/static/background-music.mp3" type="audio/mp3">
    </audio>
    <Welcome/>
</main>

<style>

@font-face {
    font-family: 'Fredoka';
    font-style: normal;
    font-weight: 600;
    src: url('/static/Fonts/FredokaOne-Regular.ttf'); /* IE9 Compat Modes */
    src:
        /* IE6-IE8 */ url('/static/Fonts/FredokaOne-Regular.ttf') format('ttf'),
        /* Super Modern Browsers */ url('/static/Fonts/FredokaOne-Regular.ttf') format('ttf'),
        /* Modern Browsers */ url('/static/Fonts/FredokaOne-Regular.ttf') format('truetype')
}

    .content_displayer{
        position: fixed;
        width: 100%;
        height: 85vh;
        overflow-y: scroll;
        font-family:'Courier New', Courier, monospace;
        color: white;

        background-image: url("/static/galaxy.gif");
        background-size:cover;
    }

    .content_displayer::-webkit-scrollbar {
    width: 8px;
    height: 10px;
    }
    .content_displayer::-webkit-scrollbar-track {
    border-radius: 10px;
    background: linear-gradient(left, #212121, #323232);
    box-shadow: 0 0 1px 1px #111;
    }
    .content_displayer::-webkit-scrollbar-thumb {
    border-radius: 10px;
    background: linear-gradient(left, #4A4A4A, #404040);
    box-shadow: inset 0 0 1px 1px #191919;
    }
    .content_displayer::-webkit-scrollbar-thumb:hover {
    background: linear-gradient(left, #555555, #4e4e4e);
    }
</style>