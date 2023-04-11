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
            <div style="font-size: 24px; font-weight: 700; margin-right: 5%">Water</div>
            {#if panelStatus=="working"}
                <Icon icon="material-symbols:water-drop" color="blue" width="32" height="32"/>
                {:else}
                <Icon icon="material-symbols:water-drop" color="gray" width="32" height="32"/>
            {/if}
        </div>
        <div class="panel-content">
            <div class="working-status">
                <div style="font-size: 16px; font-weight: 700;">status:&nbsp;</div>
                <div style={statusCSS}>{panelStatus}</div>
            </div>
            <Slider toggleText="Toggle"/>
            <div>
                <div class="interval-toggle">
                    <Slider toggleText="Interval(min) "/>
                </div>

                <div class="interval-input">
                    <div class="interval-input-input">
                        <div>On for:&nbsp;</div>
                        <input type="text">
                    </div>
                    <div class="interval-input-input">
                        <div>Every:&nbsp;</div>
                        <input type="text">
                    </div>
                </div>
 
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
        width: 300px;
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
        margin-bottom: 3%;
    }

    .interval-toggle{
        display: flex;
        flex-direction: row;
        align-items: center;
        margin-top: 3%;
    }

    .interval-input{
        display: flex;
        flex-direction: row;
        margin-top: 3%;
    }

    .interval-input-input{
        display: flex;
        flex-direction: row;
        margin-left: 5%;
    }

    .interval-input-input>input{
        width: 30px;
    }
</style>