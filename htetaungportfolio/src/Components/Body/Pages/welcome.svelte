<script>
    import Textfield from "./Components/textfield.svelte";

    export let name;
</script>

<main>
    <div>
        <h2>
            Welcome, Visitor!
        </h2>
        <h4>
        How may I address you?
        </h4>
        <Textfield placeholder="Please type here" maxlength=10 width=200 height=200/>
        <button>Proceed</button>
    </div>
</main>

<style>
    h2{
        font-size: 3em;
    }

    main{
        position: absolute;

        width: 100%;
        height:100%;

        text-align: center;
        justify-content: center;
        align-items: center;
    }

    div{

        width: 50%;
        height: 50%;
        
        position: absolute;
        top:0;
        bottom: 0;
        left: 0;
        right: 0;
    
        margin: auto;
    }
</style>