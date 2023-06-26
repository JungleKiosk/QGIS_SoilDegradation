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
                    <h3 class="title">NDVI & WDRVI</h3>
                    <button class="bg_btn mx-3" @click="toggleContent">{{ showContent ? 'Hide' : 'Show' }}</button>
                </div>
                <div v-show="showContent">
                    <p>
                        The vegetation indices are calculated from data collected by satellite or drone.
                        The electromagnetic spectrum (EM spectrum) indicates the set of all possible frequencies of
                        electromagnetic radiation. The entire spectrum is divided into the visible part of the spectrum,
                        which originates the light, and the non-visible parts with wavelengths longer or shorter than the
                        visible spectrum. <br>
                        Vegetation absorbs solar radiation in different bands, i.e. in different frequency ranges and
                        wavelengths, and re-emits a different percentage in each of them. The percentage of radiation
                        re-emitted in specific bands, such as near infrared (NIR), red (RED), and short wave infrared (Short
                        Wave Infrared – SWIR), indicates the health of the plant or water stress. <br>
                        The interpretation of the absolute value of the NDVI (Normalized Difference Vegetation Index) is
                        highly informative, since
                        allows you to immediately recognize the areas of the farm or the field that
                        have development problems. <br>
                        The NDVI is calculated according to this formula: <br>
                    <h6 class="text-center">((NIR − RED) / (NIR + RED))</h6>
                    Values can range between -1 and 1, but
                    those between -1 and 0 are typical of non-cultivated areas such as streams and zones
                    anthropogenic. In cultivated fields the values vary between 0 and 1 and each value corresponds
                    a different agronomic situation, regardless of the crop. <br>
                    The average NDVI of a field varies according to the variety and the phenological stage of the crop:
                    under equal conditions, values closer to zero mean stress and problems with vegetative development,
                    which can be caused by
                    very different factors such as, in our case, from nutritional stress and low vegetable emergence.
                    <br>
                    <hr>
                    <h4 class="title text-center">NDVI</h4>
                    Based on the crop data of the sowing period, Copernicus Sentinel-2 images relating to the periods of
                    agronomic interest are reported. <br>
                    The most present crop is corn, especially for zootechnical purposes (farms and Biogas),
                    this type of cultivation requires the chopping of the entire plant in August-September (Waxy corn).
                    <br>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/index_veg/ndvi_20062017.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/index_veg/ndvi_01092017.png" alt="">
                        </div>
                    </div>
                    <hr>
                    <h4 class="title text-center">WDRVI</h4>
                    Using the WDRVI index (Water Deficit Vegetation Index) it is possible to appreciate only the
                    well-developed vegetation and the areas of
                    greater and less vigor are more easily recognized. <br>
                    This index combines vegetation and water information to provide an estimate of plant health in relation
                    to soil water availability.
                    WDRVI is an algebraic transformation of NDVI: <br>
                    <h6 class="text-center">((0.1NIR − RED) / (0.1NIR + RED))</h6>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/index_veg/wdrvi_20062017.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/index_veg/wdrvi_01092017.png" alt="">
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
  

<style></style>

