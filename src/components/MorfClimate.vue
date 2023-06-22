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
                    highlights to the right of the Reno River, adjacent to the Valli di Comacchio. <br> <hr>
                    From ARPA data (Dext3r) of precipitation and temperature, referred to the weather station
                    Bellocchio, however, there has been a change in the last decade towards a climate of
                    Mediterranean type with summer drought in the months of June, July and August, attributable to
                    climate change. The plots was created with RStudio <a href="https://climatol.eu/" target="_blank">climatol R package</a> <br>
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
</style>

