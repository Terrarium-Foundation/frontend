<script>
    import Icon from '@iconify/svelte';
</script>

<main>
    <div style="display: flex; flex-direction: row; background: #EDF5E1; align-items: center; padding-top: 4%; padding-left: 5%; padding-bottom: 10%;   ">
        <div class="left">
            <div class="terrarium">Terrarium</div>
            <div class="terrarium-desc">welcome to the terrarium homepage. we make plant automation possible. tend to your plant from wherever you are in the world, we've got you covered. click below to get started!</div>
            <a href="/control-panel" class="get-started">
                <div style="padding-right: 10px;">let's go</div>
                <Icon icon="material-symbols:arrow-right-alt-rounded" />
            </a>
        </div>
        <div class="right">
            <img src="undraw_environment_iaus.svg" class="handholding-plant" alt="handholding-plant"/>
        </div>
    </div>
</main>

<style>

    .left{
        width: 75%;
    }

    .terrarium{
        font-size: 96px;
        font-weight: 700;
        color: #000;
        border-bottom: 5px solid black;   
        width: 80%;
        margin-bottom: 40px;
    }

    .terrarium-desc{
        font-size: 24px;
        font-weight: 400;
        color: #000;
        margin-top: 20px;
    }

    .get-started{
        display: flex;
        flex-direction: row;
        align-items: center;
        text-decoration: none;
        color: #000;
    }

    .get-started{
        transition: 1s;
        border: 3px solid yellow;
        border-radius: 10px;
        padding: 10px 20px;
        font-size: 22px;
        width: 120px;
        font-weight: 600;
        margin-top: 30px;
        margin-left: 40px;
    }

    .get-started:hover{
        transition: 1s;
        border: 3px solid yellow;
        background: rgba(255, 255, 0, 0.2);
        border-radius: 10px;
        padding: 10px 20px;
        width: 120px;
        font-size: 18px;
        font-weight: 900;
        margin-top: 30px;
        margin-left: 40px;
    }

    .handholding-plant{
        width: 70%;
        height: 70%;
        transform: scaleX(-1);
        margin-left: 35%;
    }
</style>