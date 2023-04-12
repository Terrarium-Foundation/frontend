<script>
    import DataLog from "$lib/data-log.svelte";
    import Slider from "$lib/slider.svelte";
    import TogglePanel from "$lib/toggle-panel.svelte";
    import WaterPanel from "$lib/water-panel.svelte";

    import axios from "axios";
    import { onMount } from "svelte";

    var toggleState = false;

    onMount(async()=>{
        axios.get("http://localhost:4000/state/getstate")
            .then((res)=>{
                console.log(res.data)
                if(res.data.autopilot==="on"){toggleState=true;}
                else{toggleState=false;}
            })
    })
</script>

<main style="background: #EDF5E1; padding-left: 5%;">
    <div class="autopilot">
        <Slider toggleText="Autopilot" type="autopilot" fontSize="28px" ariaExpanded={toggleState}/>
    </div>
    <div class="panels">
        <TogglePanel/>
        <div class="sep"></div>
        <WaterPanel/>
    </div>
    <DataLog/>
    <div class="fill"></div>
</main>

<style>

    .autopilot{
        padding-top: 1%;
        margin-bottom: 1%;
    }

    .panels{
        display: flex;
        flex-direction: row;
        margin-bottom: 3%;
    }
    
    .sep{
        width: 10%;
    }

    .fill{
        padding-bottom: 8%;
    }
</style>