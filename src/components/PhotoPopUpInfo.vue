<template>
  <div>
    <div
      class="modal fade"
      id="exampleModalCenter"
      tabindex="-1"
      role="dialog"
      aria-labelledby="exampleModalCenterTitle"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-xl modal-dialog-centered" role="document">
        <div class="modal-content">
          <div></div>
          <b-img :src="locationOnDisc" fluid alt="Bild"></b-img>
          <b-tabs content-class="mt-3">
            <div class="modal-body"></div>
            <b-tab title="Beskrivning" active>
              <p>Bildens textbeskrivning:</p></b-tab
            >
            <b-tab title="Specifikation"
              ><ul>
                <li>Titel:</li>
                <li>Fotograf:</li>
                <li>Format:</li>
                <li>Version av formatet:</li>
                <li>Bredd:</li>
                <li>Höjd:</li>
                <li>Filstorlek:</li>
                <li>Upplösning:</li>
                <li>Kamera:</li>
                <li>GPS-koordinater:</li>
                <li>Redigerad/Ej redigerad:</li>
                <li>Originalbild:</li>
              </ul>
            </b-tab>
            <b-tab title="Nyckelord"><p>Nyckelord</p></b-tab>
            <b-tab title="Publikationer"><p>Publikationer</p></b-tab>
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
</template>

<script>
export default {
  name: "PopUpInfo",
  props: ["locationOnDisc"],
  computed: {
    modalId() {
      return `modal-${this.id}`;
    }
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