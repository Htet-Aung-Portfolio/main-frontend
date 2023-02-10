<script>
    export let placeholder = "";
    export let value = "";
    export let maxlength = 0;

    export let width = 100;
    export let height = 100;

    function OnValueChanged(){
        console.log("Hello World!");
        let beat = new Audio("/static/keyboard.mp3");
        beat.play();
    }
</script>

<main>
    <input type="text" placeholder={placeholder} maxlength={maxlength} on:change={()=>{OnValueChanged()}} on:input={()=>{OnValueChanged()}} width={width} height={height}/>
</main>

<style>
    input{
        text-align: center;

        background-color: rgba(0, 0, 0, 0);
        color: white;
        border: 0;
        border-bottom: 2px solid white;
    }

    input::selection{
        border: 0;
    }

    input::placeholder{
        color: white;
    }

</style>