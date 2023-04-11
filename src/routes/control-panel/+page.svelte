<script>
    import DataLog from "$lib/data-log.svelte";
import Slider from "$lib/slider.svelte";
    import TogglePanel from "$lib/toggle-panel.svelte";
    import WaterPanel from "$lib/water-panel.svelte";

</script>

<main style="background: #EDF5E1; padding-left: 5%;">
    <div class="autopilot">
        <Slider toggleText="Autopilot" fontSize="28px"/>
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