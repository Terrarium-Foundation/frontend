<script>

    import axios from "axios";

    export var ariaExpanded = false;
    export var toggleText = "";
    export var fontSize = "";
    export var type = "";

    const handleToggle=(stateType)=>{
        if(ariaExpanded){
            axios.post("http://localhost:4000/state/updatestate", {toggle: stateType, action: "off", prev: "on"}).then((res)=>{
                console.log(res.data);
                ariaExpanded=false;
            }, (error)=>{
                console.log(error);
            })
        }
        else{
            axios.post("http://localhost:4000/state/updatestate", {toggle: stateType, action: "on", prev: "off"}).then((res)=>{
                console.log(res.data);
                ariaExpanded=true;
            }, (error)=>{
                console.log(error);
            })
        }
    }

</script>

<div>
    <div class="slider">
        <div class="toggle-text" style="font-size: {fontSize}">{toggleText}</div>
        <button class="outer-slider" aria-expanded={ariaExpanded} on:click={()=>{handleToggle(type)}}>
            <div class="slider-ball" aria-expanded={ariaExpanded}></div>
        </button>
    </div>
</div>

<style>

    .slider{
        display: flex;
        flex-direction: row;
        align-items: center;
    }

    .toggle-text{
        margin-right: 10px;
        font-size: 16px;
        font-weight: 700;
    }

    .outer-slider[aria-expanded="false"]{
        background: red;
        border-radius: 25px;
        display: flex;
        align-items: center;
        border: none;
    }

    .slider-ball[aria-expanded="false"]{
        background: white;
        width:25px;
        height: 25px;
        margin: 3px 25px 3px 0px;
        border-radius: 100%;
        float: left;
        transition: 0.5s;
    }

    .outer-slider[aria-expanded="true"]{
        background: green;
        border-radius: 25px;
        display: flex;
        align-items: center;
        border: none;
    }

    .slider-ball[aria-expanded="true"]{
        background: white;
        width: 25px;
        height: 25px;
        margin: 3px 0px 3px 25px;
        border-radius: 100%;
        float: right;
        transition: 0.5s;
    }
</style>