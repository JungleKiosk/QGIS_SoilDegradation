<script>
export default {
    data() {
        return {
            showContent: false, // Inizialmente nascondi il contenuto
        };
    },
    methods: {
        toggleContent() {
            this.showContent = !this.showContent; // Inverte lo stato di visualizzazione del contenuto
        },
    },
};
</script>


<template>
    <div class="container my-5 txt_jumbo ">
        <div class="row justify-content-center">
            <div class="col-12 col-lg-6 col-md-6 bg_item rounded-4">
                <div class="d-flex align-items-center justify-content-between p-3">
                    <h3 class="title">Morphology & Climatic</h3>
                    <button class="bg_btn mx-3" @click="toggleContent">{{ showContent ? 'Hide' : 'Show' }}</button>
                </div>
                <div v-show="showContent">
                    <p>
                        The Digital Terrain Model derived (DTM) from LIDAR processing shows the presence of areas below sea
                        level.
                        Altitudes higher than 1 m a.s.l. they extend laterally to the Reno drainage channel
                        right which in the past hosted the ancient course of the river Lamone frequently
                        hit by floods. <br>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/lidar/lidar_dtm.png" alt="">
                        </div>
                    </div>
                    It is therefore possible to evaluate the morphologically more depressed areas between the two dunes
                    coastal, parallel to the coast line. The area of greatest depression to the north is
                    highlights to the right of the Reno River, adjacent to the Valli di Comacchio. <br>
                    <hr>
                    From ARPA data (Dext3r) of precipitation and temperature, referred to the weather station
                    Bellocchio, however, there has been a change in the last decade towards a climate of
                    Mediterranean type with summer drought in the months of June, July and August, attributable to
                    climate change. The monthly cumulatives in Gaussen-Bagnouls plots show the increase in the dry period
                    between June and July:
                    higher temperatures
                    and less rainfall. <br>
                    The plots was created with RStudio <a href="https://climatol.eu/" target="_blank">climatol R package</a>
                    <br>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/lidar/dexter_66_00.jpeg" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/lidar/dexter_00_10.jpeg" alt="">
                        </div>
                    </div>

                    As previously mentioned, the data on which the analysis was carried out refer to the period 2016-2017,
                    years in which there was a long drought throughout the Emilia-Romagna region.
                    Indeed, the shortage of rains began in October 2016 to September 2017. <br>
                    <hr>
                    The average rainfall expected in the period October-May, according to rainfall historians, is between
                    500 and 600 mm, while the 2016-2017 period recorded trends between 300-400 in the coastal areas between
                    Ferrara
                    and Rimini. <br>
                    For analytical purposes, the rainfall analyzes relating to the winter period are reported: December 2016
                    - March 2017 and the summer period June 2017 - September 2017. <br>
                    The analyzes were carried out in Google Earth Engine environment using the <br>
                    <a href="https://www.nature.com/articles/sdata201566" target="_blank">
                        CHIRPS Daily collection: Climate Hazards Group InfraRed Precipitation With Station Data (Version 2.0
                        Final).
                    </a>

                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/prec/winter_prec.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/prec/summer_prec.png" alt="">
                        </div>
                    </div>

                    It is noted that the winter period is characterized by low levels of precipitation, even lower than in
                    summer, this implies a very low useful soil reserve to cope with the hottest season, which together with
                    the scarce summer rainfall determine the state of drought.
                    It is noted that in the province of Ravenna, where the study area is located, the precipitation values
                    are the lowest.
                    Below are the graphs of the average rainfall for each province.
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 zoom_plots">
                            <img class="rounded-3" src="./../assets/img/qgis/prec/winter_plot_region_ER_2016_2017.png"
                                alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 zoom_plots">
                            <img class="rounded-3" src="./../assets/img/qgis/prec/summer_plot_region_ER_2017.png" alt="">
                        </div>
                    </div>

                    </p>

                    <div class="end_soiltext p-3">
                        <a href="#goup">^ Go Up ^</a>
                        <button class="bg_btn mx-3" @click="toggleContent">{{ showContent ? 'Hide' : '' }}</button>
                    </div>


                </div>
            </div>
        </div>
    </div>
</template>
  

<style>
.end_soiltext a {
    text-decoration: none;
    color: #aaaaaa;
}

a {
    color: #f2b91e;
    text-decoration: underline;
}

.zoom_plots {
    transition: transform 0.2s ease-in-out;
    transform-origin: center center;
}

.zoom_plots:hover {
    transform: scale(1.75);
    border: 0;
}
</style>

