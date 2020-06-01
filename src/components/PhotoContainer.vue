<template>
  <div>
    <b-col>
      <b-card
        :title="oportunityDescription"
        :img-src="locationOnDisc"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
      >
        <b-card-text>
          Some quick example text to build on the card title and make up the
          bulk of the card's content.
        </b-card-text>
        <b-button
          v-b-tooltip.hover
          title="Bildinformation"
          v-b-modal="modalId"
          variant="primary"
          data-toggle="modal"
          data-target="#exampleModalCenter"
          >Info</b-button
        >
      </b-card>
    </b-col>
    <div>
      <div
        class="modal fade"
        id="exampleModalCenter"
        tabindex="-1"
        role="dialog"
        aria-labelledby="exampleModalCenterTitle"
        aria-hidden="true"
      >
        <div
          class="modal-dialog modal-xl modal-dialog-centered"
          role="document"
        >
          <div class="modal-content">
            <div></div>
            <b-img :src="locationOnDisc" fluid alt="Bild"></b-img>
            <b-tabs content-class="mt-3">
              <div class="modal-body"></div>
              <b-tab title="Beskrivning" active>
                <p>{{ oportunityDescription }}</p>
                <p>{{ photoDescription }}</p></b-tab
              >
              <b-tab title="Specifikation"
                ><ul>
                  <li>Titel: {{ }} </li>
                  <li>Fotograf: {{ fName }} {{ lName }}</li>
                  <li>Format: {{ fileFormat }}</li>
                  <li>Bredd: {{ width }}</li>
                  <li>Höjd: {{ height }}</li>
                  <li>Filstorlek: {{ fileSiz }}</li>
                  <li>Upplösning: {{ resolution }}</li>
                  <li>Kamera: {{ camera }}</li>
                  <li>GPS-koordinater: {{ coordinates }}</li>
                  <li>Redigerad/Ej redigerad: {{ }}</li>
                  <li>Originalbild: {{ original }}</li>
                  <li>Införskaffad genom: {{ aquiredThrough }}</li>
                  <li>Max antal användningar: {{ maxUse }}</li>
                  <li>Använd: {{ used }}</li>
                  <li>Pris: {{ price }}</li>
                </ul>
              </b-tab>
              <b-tab title="Nyckelord"
                ><p>{{ keywords }}</p></b-tab
              >
              <b-tab title="Publikationer"
                ><p>{{ publishings }}</p></b-tab
              >
              <b-tab title="Versioner"><p>Versioner</p></b-tab>
            </b-tabs>
            <div class="modal-footer">
              <button
                type="button"
                class="btn btn-outline-info waves-effect ml-auto"
                data-dismiss="modal"
              >
                Close
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PhotoContainer",
  props: [
    "aquiredThrough",
    "camera",
    "coordinates",
    "datetime",
    "fName",
    "fileFormat",
    "fileSize",
    "height",
    "keywords",
    "lName",
    "locationOnDisc",
    "maxUse",
    "oportunityDescription",
    "original",
    "photoDescription",
    "piNo",
    "price",
    "publishings",
    "resolution",
    "used",
    "width"
  ],
  computed: {
    modalId() {
      return `modal-${this.id}`;
    }
  },
  data: function() {
    return {};
  }
};
</script>

<style lang="scss" scoped>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
</style>
