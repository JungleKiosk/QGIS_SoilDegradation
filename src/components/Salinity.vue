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
                    <h3 class="title">Salinity</h3>
                    <button class="bg_btn mx-3" @click="toggleContent">{{ showContent ? 'Hide' : 'Show' }}</button>
                </div>
                <div v-show="showContent">
                    <p>
                        The phenomenon consists in the progressive accumulation of soluble salts in the soil. It can be
                        divided into two types:
                    <ul>
                        <li>Primary salinity: of natural origin</li>
                        <li>Secondary salinity: induced by human</li>
                    </ul>
                    The causes of secondary salinity can be agricultural practices
                    that are not adapted to the natural context <br>
                    (irrigation with unsuitable water, abuse of mineral fertilisers, excessive pumping from groundwater,
                    cementing of riverbeds). <br>
                    Accumulation processes occur particularly in coastal agricultural plains,
                    which by their nature are sensitive to marine intrusion phenomena, but also in
                    many inland irrigated agricultural plains where the risk of salinisation is common
                    due to the use of poor quality water, often aggravated by the presence of soil
                    with properties that limit good leaching of salts, such as the presence of
                    impermeable horizons and the unfavorable physiographic position. <br>
                    <hr>
                    <h4 class="title text-center">SAR</h4>
                    Prescription maps of the areas at risk are created: data relating to irrigation water sampling show the
                    values of sodium, calcium and magnesium (mmol/L), from which the SAR (Sodium Adsorption Ratio) can be
                    derived. <br>
                    It was deemed necessary to distinguish
                    data relating to the sampling of the WINTER months from the SUMMER ones, to appreciate the differences.
                    To classify the SAR levels IDW was used, according to the table of agricultural tolerance limits for the
                    use of irrigation water proposed by Giardini et al. (1993)

                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/salinity/sar_winter.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/salinity/sar_summer.png" alt="">
                        </div>
                    </div>
                    From the analyzes carried out, it can be seen that the irrigation water used in the company area
                    they are more saline in the winter months than in the summer months. <br>
                    This is attributable to the fact that, during the
                    summer period, the Reclamation Consortium circulates large volumes of good quality water
                    that mix with brackish water present in the canals, obtaining
                    thus water of acceptable quality for irrigation. <br>
                    Note how the pH too
                    of water increases significantly in winter.

                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/salinity/ph_winter.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/salinity/ph_summer.png" alt="">
                        </div>
                    </div>
                    <hr>
                    <h4 class="title text-center">EC</h4>
                    The electrical conductivity data in saturated paste (EC) in the soil layers 0-10, 10-30, 30-60 and
                    60-90 centimeters were processed and it was
                    developed a map to provide information on soil suitability for crops. <br>
                    To classify the EC levels IDW was used, according to the table of soil salinity classes proposed by
                    Richards and the
                    <a href="https://www.nrcs.usda.gov/sites/default/files/2022-09/The-Soil-Survey-Manual.pdf"
                        target="_blank">
                        USDA Soil Survey Manual.
                    </a> <br> <br>
                    <table>
                        <thead>
                            <tr>
                                <th>EC [dS/m]</th>
                                <th>Classes</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>&lt; 2</td>
                                <td>Non saline</td>
                            </tr>
                            <tr>
                                <td>2.1 - 4.0</td>
                                <td>Sligthly saline</td>
                            </tr>
                            <tr>
                                <td>4.1 - 8.0</td>
                                <td>Moderately saline</td>
                            </tr>
                            <tr>
                                <td>8.0 - 16.0</td>
                                <td>Strongnly saline</td>
                            </tr>
                            <tr>
                                <td>> 16.0</td>
                                <td>Very strongly saline</td>
                            </tr>
                        </tbody>
                    </table>

                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/ec/ec_0010.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/ec/ec_1030.png" alt="">
                        </div>
                    </div>
                    Regarding the soil horizon of agricultural interest (from 0 to 30cm), the
                    most of the farm area does not present a danger of crop depression, for i
                    recorded levels of soil EC. In fact we find surfaces belonging to the second class of EC, therefore
                    values that are not too high. <br>
                    Also the pH seems to be not excessively alkaline, with values between 7.3 and 7.9
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/usda/ph_0010.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/usda/ph_1030.png" alt="">
                        </div>
                    </div>
                    However, it should be noted that with increasing depth, the surfaces belonging to the second class
                    increase, due to the proximity to the sea and the rise of the salt wedge.

                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/ec/ec_3060.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/ec/ec_6090.png" alt="">
                        </div>
                    </div>

                    Considering the territorial context and the problems previously
                    exposed, the relatively low EC values may be attributable to the continuous agricultural tillage and
                    the constant withdrawals of water for irrigation, which
                    keep soil salinity low. <br>
                    Activities of this kind could lead to soil depletion, with a constant need for large quantities of water
                    suitable for irrigation.
                    It is therefore important to evaluate the texture of the corporate surface and the
                    correlation of the EC with it and with the other field variables.
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

table {
    border-collapse: collapse;
    width: 100%;
    border: 1px solid #000;
}

th,
td {
    padding: 8px;
    border: 1px solid #000;
}
</style>

