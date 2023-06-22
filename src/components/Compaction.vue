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
                    <h3 class="title">Compaction</h3>
                    <button class="bg_btn mx-3" @click="toggleContent">{{ showContent ? 'Hide' : 'Show' }}</button>
                </div>
                <div v-show="showContent">
                    <p>
                        The compaction phenomenon is expressed when the soil particles are
                        tablets reducing the space and continuity of pores.
                        Consequently increases the
                        apparent density of the soil, as more particles are arranged in a unit of volume.
                        Heavily compacted soils have a low percentage of macropores, whereby water moves through the soil
                        when it is saturated, and this
                        it results in a lower infiltration and drainage capacity. <br>
                        Sandy soils have a lower total porosity than clayey soils, but are usually well aerated because the
                        pores are large enough to allow water to drain. The greater aeration of sandy soils is therefore
                        associated with a lower capacity
                        of water retention. Furthermore, greater aeration leads to rapid mineralization of the organic
                        substance and the consequent risk of leaching of nutrients. <br>
                        However, gas exchange slows down in compact soils, causing less aeration, with the risk of root
                        asphyxia and a loss of physiological balance of crops, with related repercussions on agricultural
                        yields. <br>
                        Therefore, it is important to maintain a balanced soil structure. <br>
                        <hr>
                    <h4 class="title text-center">Porosity</h4>
                    The porosity of a soil can be calculated from its bulk density; weight of the unit volume of soil,
                    including pore spaces, from which the water comes
                    removed by passing the sample in an oven. <br>
                    Therefore, for the purposes of this work, the porosity value was calculated for each one
                    of the sampled points, through the following formula:
                    <h4 class="text-center">Porosity = ( 1 - (DB / 2.65) * 100)</h4>
                    The distributions of the porosity classes on the company surface are shown below,
                    so as to discriminate the most degraded areas from those in better condition. This will be useful for
                    agronomic prescriptions related to crops.

                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/compaction/por_0010.png" alt="">
                        </div>
                    </div>

                    <h4 class="title text-center">Soil Texture and SOM</h4>
                    Most of the company soil has a loamy-silty (LoSa), clayey-silt (ClLo) and sandy-silt (SaLo) texture.
                    To learn more and understand how the soil texture was geolocated, click <a
                        href="https://junglekiosk.github.io/QGIS_SoilTexture/" target="_blank">here</a>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/usda/usda_0010.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/usda/usda_1030.png" alt="">
                        </div>
                    </div>
                    From the TOC data, the percentage of soil organic matter (SOM) was estimated,
                    multiplying by the conversion factor 1.724.
                    The total distribution of the SOM, throughout the territory, was first identified
                    on USDA soil texture triangle with RStudio
                    <a href="https://cran.r-project.org/web/packages/soiltexture/vignettes/soiltexture_vignette.pdf"
                        target="_blank">soil texture wizard</a>,
                    then compared with USDA grading
                    tables.
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/usda/usda_som_0010.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/usda/usda_som_1030.png" alt="">
                        </div>
                    </div>

                    <table>
                        <thead>
                            <tr>
                                <th>% SOM</th>
                                <th>Sand</th>
                                <th>Loam</th>
                                <th>Clay</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>Very low</td>
                                <td>&lt; 0.8</td>
                                <td>&lt; 1.0</td>
                                <td>&lt; 1.2</td>
                            </tr>
                            <tr>
                                <td>Low</td>
                                <td>0.8 - 1.4</td>
                                <td>1.0 - 1.8</td>
                                <td>1.2 - 2.2</td>
                            </tr>
                            <tr>
                                <td>Medium</td>
                                <td>1.5 - 2.0</td>
                                <td>1.9 - 2.5</td>
                                <td>2.3 - 3.0</td>
                            </tr>
                            <tr>
                                <td>High</td>
                                <td>> 2.0</td>
                                <td>> 2.5</td>
                                <td>> 3.0</td>
                            </tr>
                        </tbody>
                    </table> <br>
                    It can be seen that in general there is a shortage of SOM, with maximum values in the sandy fractions of
                    the first 10cm and in the clayey fractions between 10 and 30cm. The degradative phenomenon of compaction
                    triggers soil erosion and
                    decrease in SOM.








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
  

<style></style>

