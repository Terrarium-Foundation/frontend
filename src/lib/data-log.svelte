<script>
    import Icon from '@iconify/svelte';
</script>

<div>
    <div class="header">
        <Icon icon="pepicons-pop:rewind-time" />
        <div>Data last fetched:&nbsp<span class="timefetched"></span></div>
    </div>
    <div class="data-col">
        <div>
            <div>
                <Icon icon="mdi:humidity" width="24" height="24"/>
                <div class="data-reading">
                    <div>Humidity:&nbsp;</div>
                    <div class="value">6565</div>
                </div>
            </div>
            <div>
                <Icon icon="carbon:soil-moisture-field" width="24" height="24"/>
                <div class="data-reading">
                    <div>Soil Moisture:&nbsp;</div>
                    <div class="value">2421</div>
                </div>
            </div>
        </div>
        <div style="margin-left: 40px;">
            <div>
                <Icon icon="mdi:home-temperature" width="24" height="24"/>
                <div class="data-reading">
                    <div>Temperature:&nbsp;</div>
                    <div class="value">3452</div>
                </div>
            </div>
            <div>
                <Icon icon="mdi:car-light-dimmed" width="24" height="24"/>
                <div class="data-reading">
                    <div>Light Intensity:&nbsp;</div>
                    <div class="value">234</div>
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    .header{
        display: flex;
        flex-direction: row;
        align-items: center;
        font-size: 22px;
        font-weight: 700;
    }
    .header>div{
        margin-left: 1%;
    }
    .data-col{
        margin-left: 2%;
        margin-top: 1%;
        display: flex;
        flex-direction: row;
    }
    .data-col>div>div{
        display: flex;
        flex-direction: row;
        align-items: center;
        margin-bottom: 10px;
        font-size: 18px;
    }
    .data-reading{
        display: flex;
        flex-direction: row;
        margin-left: 5px;
    }
</style>