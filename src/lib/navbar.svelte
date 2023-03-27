<script>
    import Icon from '@iconify/svelte';
    export var navState = 0;
</script>

<div>
    <div class="navbar">
        <div class="nav-left">
            <img src="Terrarium-1.png" alt="terrarium-logo"/>
        </div>
        <div class="nav-spacer"></div>
        <div class="nav-right">
            <div>
                <a href="/control-panel" on:click={()=>{navState=0}}>
                    <Icon icon="ant-design:control-outlined" />
                    <div>Control Panel</div>
                </a>
            </div>
            <div>
                <a href="/data-analytics" on:click={()=>{navState=1}}>
                    <Icon icon="ion:analytics-sharp" />
                    <div>Analytics</div>
                </a>
            </div>
            <div>
                <a href="/" on:click={()=>{navState=2}}>
                    <Icon icon="material-symbols:home-outline-rounded" />
                    <div>Home</div>
                </a>
            </div>
        </div>
    </div>
</div>

<style>

    .navbar{
        display: flex;
        flex-direction: row;
        align-items: center;
        background: #EDF5E1;
    }

    .nav-left>img{
        width: 250px;
        height: 75px;
    }

    .nav-spacer{
        width: 45%;
    }

    .nav-right{
        display: flex;
        flex-direction: row;
    }

    .nav-right>div{
        display: flex;
        flex-direction: row;
        align-items: center;
        margin-left: 30px;
    }

    .nav-right>div>a{
        color: black;
        text-decoration: none;
        display: flex;
        flex-direction: row;
        align-items: center;
        font-weight: 600;
        font-size: 16px;
    }

    .nav-right>div>a>div{
        margin-left: 10px;
    }

</style>