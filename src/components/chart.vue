<template>
    <div class="chart -mt-5">
        <apexchart width="100%" type="area" height="90" :options="options" :series="series"></apexchart>
    </div>
</template>

<script>
    import VueApexCharts from 'vue-apexcharts'
    export default {
        components: {
            'apexchart': VueApexCharts,
        },
        props: ['weeklyGraph'],
        data() {
            return {
                options: {
                    chart: {
                        height: 20,
                        offsetY: 20,
                        parentHeightOffset: 0,
                        id: 'vuechart-example',
                        zoom: {
                            enabled: false
                        },
                        toolbar: {
                            show: false
                        },
                    },
                    xaxis: {
                        grid: {
                            padding: {
                                left: 100,
                                right: 0
                            }
                        },
                        labels: {
                            show: false
                        },
                        axisBorder: {
                            show: false
                        },
                        axisTicks: {
                            show: false
                        },
                        categories: [
                            "01 Jan",
                            "02 Jan",
                            "03 Jan",
                            "04 Jan",
                            "05 Jan",
                            "06 Jan",
                        ]
                    },
                    yaxis: {
                        min: 0,
                        show: true,
                        labels: {
                            show: false
                        },
                        axisBorder: {
                            show: false
                        },
                        axisTicks: {
                            show: false
                        },
                        grid: {
                            padding: {
                                left: 0,
                                right: 0,
                            }
                        },
                    },
                    stroke: {
                        curve: 'smooth',
                    },
                    
                                        colors: ['#34c66e', '#231E3D'],
                    fill: {
                        type: 'gradient',
                        gradient: {
                            shade: 'dark',
                            type: "vertical",
                            shadeIntensity: 0.5,
                            gradientToColors: undefined, // optional, if not defined - uses the shades of same color in series
                            inverseColors: true,
                            opacityFrom: 0.5,
                            opacityTo: 0.1,
                            stops: [0, 90, 100],
                            colorStops: []
                        }
                    },
                    dataLabels: {
                        enabled: false
                    },
                    grid: {
                        show: false,
                        padding: {
                            left: -10,
                            right: 0,
                            bottom:0
                        }
                    }
                },
                series: [{
                    name: 'series-1',
                    data: this.weeklyGraph
                }]
            }
        }
    }
</script>