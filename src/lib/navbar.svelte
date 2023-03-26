<script>
    import Icon from '@iconify/svelte';
</script>

<div>
    <div class="navbar">
        <div class="nav-left">
            <img src="Terrarium-1.png" alt="terrarium-logo"/>
        </div>
        <div class="nav-spacer"></div>
        <div class="nav-right">
            <div>
                <Icon icon="ant-design:control-outlined" />
                <div>Control Panel</div>
            </div>
            <div>
                <Icon icon="ion:analytics-sharp" />
                <div>Analytics</div>
            </div>
            <div>
                <Icon icon="material-symbols:home-outline-rounded" />
                <div>Home</div>
            </div>
        </div>
    </div>
</div>

<style>

    .navbar{
        display: flex;
        flex-direction: row;
        align-items: center;
        font-weight: 600;
        font-size: 16px;
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

    .nav-right>div>div{
        margin-left: 10px;
    }

</style>