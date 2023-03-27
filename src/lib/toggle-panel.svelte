<script>
    import Slider from "./slider.svelte";
    import Icon from '@iconify/svelte';

    var panelStatus = "working"
    var statusCSS = ""
    var showInterval = false

    function handleInterval(){
        if(showInterval){
            showInterval=false;
        }
        else{
            showInterval=true;
        }
    }

    if(panelStatus=="working"){
        statusCSS = "color: green"
    }
    else{
        statusCSS = "color: red"
    }

</script>

<div>
    <div class="toggle-panel">
        <div class="panel-header">
            <div>Light</div>
            {#if panelStatus=="working"}
                <Icon icon="ph:sun-bold" color="gray" width="32" height="32"/>
                {:else}
                <Icon icon="ph:sun-bold" color="yellow" width="32" height="32"/>
            {/if}
        </div>
        <div class="panel-content">
            <div class="working-status">
                <div>Status: </div>
                <div style={statusCSS}>{panelStatus}</div>
            </div>
            <Slider toggleText="Toggle"/>
            <div>
                <div class="interval-toggle">
                    <div>Interval(min)</div>
                    <input type="checkbox" class="interval-button" on:click={handleInterval}>
                </div>
                {#if showInterval}
                    <div class="interval-input">
                        <div class="interval-input-input">
                            <div>On for:</div>
                            <input type="text">
                        </div>
                        <div class="interval-input-input">
                            <div>Every:</div>
                            <input type="text">
                        </div>
                    </div>
                {/if}
            </div>
        </div>
    </div>
</div>

<style>

    .panel-header{
        display: flex;
        flex-direction: row;
        align-items: center;
    }

    .toggle-panel{
        margin: 10px;
        width: 200px;
    }

    .panel-content{
        margin: 10px;
        padding: 10px;
        width: 100%;
        border-radius: 10px;
        border: 5px solid #fbee99;
    }

    .working-status{
        display: flex;
        flex-direction: row;
    }

    .interval-toggle{
        display: flex;
        flex-direction: row;
        align-items: center;
    }

    .interval-button{
        background: transparent;
        border: none;
    }

    .interval-input{
        display: flex;
        flex-direction: row;
    }

    .interval-input-input{
        display: flex;
        flex-direction: row;
    }

    .interval-input-input>input{
        width: 30px;
    }
</style>