<script>
    export let content = "";

    function playhoversound(){
        let beat = new Audio("/static/Hover-Sound.mp3");
        beat.play();
    }
</script>

<main>
    <button on:mouseenter={()=>{playhoversound()}}>
        {content}
    </button>
</main>

<style>
    button{
        border-radius: 20%;
        color: white;
        background-color: rgba(0,0,0,0);
        transition-duration: 0.25s;
    }

    button:hover{
        background-color: rgb(87, 1, 98);
        border-color: rgba(0,0,0,0);
    }
</style>