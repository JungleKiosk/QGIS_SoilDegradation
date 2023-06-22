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
                    <h3 class="title">Agronomic Aspects</h3>
                    <button class="bg_btn mx-3" @click="toggleContent">{{ showContent ? 'Hide' : 'Show' }}</button>
                </div>
                <div v-show="showContent">
                    <p>
                        In basically alkaline soils, such as the one in question, the concentration of limestone
                        active (CaCO3) can constitute more than half of the solid fraction of the soil contributing in
                        decisive way to define its properties. <br>
                        On the other hand, in acid soils, it is rarely present and in
                        any case in large quantities
                        low, so much so that when the pH is lower than 6.5 the limestone determination can
                        be left out. <br>
                        The presence of limestone in the soil, within certain limits, is to be considered positive for the
                        nutritional function performed by calcium in relation to plants and for their effects
                        favorable on the structure and mineralization of organic substances. <br>
                        However, when it is present in excessive quantities and above all in mineralogical forms
                        very active, the typical drawbacks of alkaline soils may occur (e.g
                        example insolubilization of P and Fe). <br>
                        <hr>
                    <h4 class="title text-center">Total CaCO3</h4>
                    The reference classes have a different meaning from those used for nutrients since
                    increasing quantities of limestone, especially if active, do not have the positive effect of one
                    greater availability of fertilizing elements but on the contrary they are an indication of a
                    negative situation due to the insolubilization of some essential nutrients for
                    normal plant growth. <br> <br>

                    <table>
                        <thead>
                            <tr>
                                <th>Total CaCO3 [%]</th>
                                <th>Classes</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>&lt; 1</td>
                                <td>Not calcareous</td>
                            </tr>
                            <tr>
                                <td>1 - 5</td>
                                <td>Sligthly calcareous</td>
                            </tr>
                            <tr>
                                <td>5 - 10</td>
                                <td>Moderately calcareous</td>
                            </tr>
                            <tr>
                                <td>10 - 25</td>
                                <td>Very calcareous</td>
                            </tr>
                            <tr>
                                <td>25 - 40</td>
                                <td>Strongnly calcareous</td>
                            </tr>
                            <tr>
                                <td>> 40</td>
                                <td>Very strongly calcareous</td>
                            </tr>
                        </tbody>
                    </table>

                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/compaction/caco3_0010.png" alt="">
                        </div>
                    </div>
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/compaction/caco3_0010.png" alt="">
                        </div>
                    </div>

                    The total limestone content affects, just like the clay, the bioavailability of the minerals
                    elements for crops; therefore, the choice of resistant varieties and rootstocks and the speed
                    degradation of soil organic matter. <br>
                    <hr>
                    <h4 class="title text-center">K2</h4>
                    The higher the amount of limestone present in the soil, the greater the inertia of the soil towards the
                    transformation processes of organic compounds. <br>
                    The speed of this process is described by the mineralization coefficient (K2)
                    which indicates the amount of SOM that is consumed on average, or better, is mineralized in
                    one year. <br>
                    The annual mineralization coefficient K2 (Rémy and Marin-Laflèche, 1974) is given by: <br> <br>
                    <h6 class="text-center">K2 [%] = 1200 * (1/(%Clay + 20)) * (1/(%CaCO3 + 20)) </h6>
                    This coefficient varies according to the soil characteristics and is influenced by the climate and soil
                    management. It assumes high values for light and oxygenated soils, and lower values for heavy ones.
                    <div class="row justify-content-center my-3">
                        <div class="col-12 col-lg-12 col-md-8 ">
                            <img class="rounded-3" src="./../assets/img/qgis/compaction/k2_0010.png" alt="">
                        </div>
                    </div>
                    Based on the works of various authors, the average value of K2 varies from &lt; 1% for soils
                    clayey, up to 2.2% for sandy soils. <br>
                    In this case, values are recorded which
                    even reach 20%. This is because from the maps reported so far we observe a
                    very aerated soil (high porosity), with very little SOM and moreover soils
                    constantly processed for agricultural use. <br>
                    In this case, values are recorded which
                    even reach 20%. This is because, from the maps reported so far, we observe a very airy soil (high
                    porosity), with very little SOM and, moreover, soils constantly worked for agricultural use.
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

