<template>
    <div id="app-container">
        <DxDataGrid id="dataGrid" :allow-column-reordering="true"> </DxDataGrid>

        <DxChart id="chart" :data-source="populationData" title="World Population by Decade">
            <DxArgumentAxis :tick-interval="10">
                <DxLabel format="decimal" />
            </DxArgumentAxis>
            <DxSeries type="bar" />
            <DxLegend :visible="false" />
        </DxChart>
    </div>
</template>

<script lang="ts" setup>
    import { ref } from 'vue'
    import { DxDataGrid } from 'devextreme-vue/data-grid'
    import DxChart, { DxArgumentAxis, DxLegend, DxLabel, DxSeries } from 'devextreme-vue/chart'

    const populationData = ref([
        {
            arg: 1960,
            val: 3032019978,
        },
        {
            arg: 1970,
            val: 3683676306,
        },
        {
            arg: 1980,
            val: 4434021975,
        },
        {
            arg: 1990,
            val: 5281340078,
        },
        {
            arg: 2000,
            val: 6115108363,
        },
        {
            arg: 2010,
            val: 6922947261,
        },
        {
            arg: 2020,
            val: 7795000000,
        },
    ])
</script>

<style>
    #dataGrid {
        height: 500px;
    }
</style>
